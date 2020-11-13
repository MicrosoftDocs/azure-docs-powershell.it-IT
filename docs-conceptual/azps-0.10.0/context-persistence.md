---
title: Contesti e credenziali di accesso di Azure
description: Informazioni su come riutilizzare le credenziali di Azure e altre informazioni in più sessioni di PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: be9113ab1ad6a359832634ae2c21fd177b09318f
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2020
ms.locfileid: "93410469"
---
# <a name="azure-powershell-context-objects"></a><span data-ttu-id="313ae-103">Oggetti contesto di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="313ae-103">Azure PowerShell context objects</span></span>

<span data-ttu-id="313ae-104">Azure PowerShell usa gli _oggetti contesto di Azure PowerShell_ (contesti di Azure) per memorizzare informazioni su sottoscrizioni e autenticazione.</span><span class="sxs-lookup"><span data-stu-id="313ae-104">Azure PowerShell uses _Azure PowerShell context objects_ (Azure contexts) to hold subscription and authentication information.</span></span> <span data-ttu-id="313ae-105">Nel caso di più sottoscrizioni, i contesti di Azure consentono di selezionare quella in cui eseguire i cmdlet di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="313ae-105">If you have more than one subscription, Azure contexts let you select the subscription to run Azure PowerShell cmdlets on.</span></span> <span data-ttu-id="313ae-106">I contesti di Azure possono anche essere usati per archiviare informazioni di accesso tra più sessioni di PowerShell e per eseguire attività in background.</span><span class="sxs-lookup"><span data-stu-id="313ae-106">Azure contexts are also used to store sign-in information across multiple PowerShell sessions and run background tasks.</span></span>

<span data-ttu-id="313ae-107">Questo articolo riguarda i contesti di Azure, non la gestione di sottoscrizioni o account.</span><span class="sxs-lookup"><span data-stu-id="313ae-107">This article covers managing Azure contexts, not the management of subscriptions or accounts.</span></span> <span data-ttu-id="313ae-108">Per informazioni su gestione degli utenti, sottoscrizioni, tenant o account, vedere la documentazione di [Azure Active Directory](/azure/active-directory).</span><span class="sxs-lookup"><span data-stu-id="313ae-108">If you're looking to manage users, subscriptions, tenants, or other account information, see the [Azure Active Directory](/azure/active-directory) documentation.</span></span> <span data-ttu-id="313ae-109">Per informazioni sull'uso di contesti per l'esecuzione in background di attività parallele, vedere [Usare i cmdlet di Azure PowerShell in processi di PowerShell](using-psjobs.md) dopo aver acquisito familiarità con i contesti di Azure.</span><span class="sxs-lookup"><span data-stu-id="313ae-109">To learn about using contexts for running background or parallel tasks, see [Use Azure PowerShell cmdlets in PowerShell jobs](using-psjobs.md) after becoming familiar with Azure contexts.</span></span>

## <a name="overview-of-azure-context-objects"></a><span data-ttu-id="313ae-110">Panoramica degli oggetti contesto di Azure</span><span class="sxs-lookup"><span data-stu-id="313ae-110">Overview of Azure context objects</span></span>

<span data-ttu-id="313ae-111">I contesti di Azure sono oggetti di PowerShell che rappresentano la sottoscrizione attiva in cui eseguire i comandi e le informazioni di autenticazione necessarie per connettere Azure al cloud.</span><span class="sxs-lookup"><span data-stu-id="313ae-111">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="313ae-112">Con i contesti di Azure, non è necessario ripetere l'autenticazione dell'account in Azure PowerShell ogni volta che si cambia sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="313ae-112">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="313ae-113">Un contesto di Azure è costituito da:</span><span class="sxs-lookup"><span data-stu-id="313ae-113">An Azure context consists of:</span></span>

* <span data-ttu-id="313ae-114">L' _account_ usato per accedere ad Azure con [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="313ae-114">The _account_ that was used to sign in to Azure with [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).</span></span> <span data-ttu-id="313ae-115">I contesti di Azure considerano gli utenti, gli ID applicazione e le entità servizio allo stesso modo dal punto di vista di un account.</span><span class="sxs-lookup"><span data-stu-id="313ae-115">Azure contexts treat users, application IDs, and service principals the same from an account perspective.</span></span>
* <span data-ttu-id="313ae-116">La _sottoscrizione_ attiva, un contratto di servizi stipulato con Microsoft per la creazione e l'esecuzione delle risorse di Azure, che sono associate a un _tenant_.</span><span class="sxs-lookup"><span data-stu-id="313ae-116">The active _subscription_ , a service agreement with Microsoft to create and run Azure resources, which are associated with a _tenant_.</span></span> <span data-ttu-id="313ae-117">I tenant vengono spesso citati come _organizzazioni_ nella documentazione e durante l'uso di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="313ae-117">Tenants are often referred to as _organizations_ in documentation or when working with Active Directory.</span></span>
* <span data-ttu-id="313ae-118">Un riferimento a una _cache del token_ , un token di autenticazione archiviato per l'accesso al cloud di Azure.</span><span class="sxs-lookup"><span data-stu-id="313ae-118">A reference to a _token cache_ , a stored authentication token for accessing an Azure cloud.</span></span> <span data-ttu-id="313ae-119">La posizione di archiviazione e la durata del periodo di conservazione di tale token vengono definite dalle [impostazioni di salvataggio automatico dei contesti](#save-azure-contexts-across-powershell-sessions).</span><span class="sxs-lookup"><span data-stu-id="313ae-119">Where this token is stored and how long it persists for is determined by the [context autosave settings](#save-azure-contexts-across-powershell-sessions).</span></span>

<span data-ttu-id="313ae-120">Per altre informazioni, vedere [Terminologia di Azure Active Directory](/azure/active-directory/fundamentals/active-directory-whatis#terminology).</span><span class="sxs-lookup"><span data-stu-id="313ae-120">For more information on these terms, see [Azure Active Directory Terminology](/azure/active-directory/fundamentals/active-directory-whatis#terminology).</span></span> <span data-ttu-id="313ae-121">I token di autenticazione usati dai contesti di Azure sono uguali ad altri token archiviati che fanno parte di una sessione persistente.</span><span class="sxs-lookup"><span data-stu-id="313ae-121">Authentication tokens used by Azure contexts are the same as other stored tokens that are part of a persistent session.</span></span>

<span data-ttu-id="313ae-122">Quando si accede con `Connect-AzAccount`, viene creato almeno un contesto di Azure per la sottoscrizione predefinita.</span><span class="sxs-lookup"><span data-stu-id="313ae-122">When you sign in with `Connect-AzAccount`, at least one Azure context is created for your default subscription.</span></span> <span data-ttu-id="313ae-123">L'oggetto restituito da `Connect-AzAccount` è il contesto di Azure predefinito usato per il resto della sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="313ae-123">The object returned by `Connect-AzAccount` is the default Azure context used for the rest of the PowerShell session.</span></span>

## <a name="get-azure-contexts"></a><span data-ttu-id="313ae-124">Ottenere i contesti di Azure</span><span class="sxs-lookup"><span data-stu-id="313ae-124">Get Azure contexts</span></span>

<span data-ttu-id="313ae-125">I contesti di Azure disponibili vengono recuperati con il cmdlet [Get-AzContext](/powershell/module/az.accounts/get-azcontext).</span><span class="sxs-lookup"><span data-stu-id="313ae-125">Available Azure contexts are retrieved with the [Get-AzContext](/powershell/module/az.accounts/get-azcontext) cmdlet.</span></span> <span data-ttu-id="313ae-126">Per elencare tutti i contesti disponibili, usare `-ListAvailable`:</span><span class="sxs-lookup"><span data-stu-id="313ae-126">List all of the available contexts with `-ListAvailable`:</span></span>

```azurepowershell-interactive
Get-AzContext -ListAvailable
```

<span data-ttu-id="313ae-127">Oppure ottenere un contesto per nome:</span><span class="sxs-lookup"><span data-stu-id="313ae-127">Or get a context by name:</span></span>

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
```

<span data-ttu-id="313ae-128">I nomi dei contesti possono essere diversi dal nome della sottoscrizione associata.</span><span class="sxs-lookup"><span data-stu-id="313ae-128">Context names may be different from the name of the associated subscription.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="313ae-129">I contesti di Azure disponibili __non__ corrispondono sempre alle sottoscrizioni disponibili,</span><span class="sxs-lookup"><span data-stu-id="313ae-129">The available Azure contexts __aren't__ always your available subscriptions.</span></span> <span data-ttu-id="313ae-130">ma rappresentano solo informazioni archiviate in locale.</span><span class="sxs-lookup"><span data-stu-id="313ae-130">Azure contexts only represent locally-stored information.</span></span> <span data-ttu-id="313ae-131">Per ottenere le sottoscrizioni, usare il cmdlet [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription).</span><span class="sxs-lookup"><span data-stu-id="313ae-131">You can get your subscriptions with the [Get-AzSubscription](/powershell/module/Az.Accounts/Get-AzSubscription) cmdlet.</span></span>

## <a name="create-a-new-azure-context-from-subscription-information"></a><span data-ttu-id="313ae-132">Creare un nuovo contesto di Azure dalle informazioni della sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="313ae-132">Create a new Azure context from subscription information</span></span>

<span data-ttu-id="313ae-133">Il cmdlet [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) consente sia di creare nuovi contesti di Azure sia di impostarli come contesto attivo.</span><span class="sxs-lookup"><span data-stu-id="313ae-133">The [Set-AzContext](/powershell/module/Az.Accounts/Set-AzContext) cmdlet is used to both create new Azure contexts and set them as the active context.</span></span>
<span data-ttu-id="313ae-134">Il modo più semplice per creare un nuovo contesto di Azure consiste nell'usare le informazioni della sottoscrizione esistenti.</span><span class="sxs-lookup"><span data-stu-id="313ae-134">The easiest way to create a new Azure context is to use existing subscription information.</span></span> <span data-ttu-id="313ae-135">Il cmdlet è progettato per configurare un nuovo contesto di Azure con l'oggetto output di `Get-AzSubscription` come valore della pipeline:</span><span class="sxs-lookup"><span data-stu-id="313ae-135">The cmdlet is designed to take the output object from `Get-AzSubscription` as a piped value and configure a new Azure context:</span></span>

```azurepowershell-interactive
Get-AzSubscription -SubscriptionName 'MySubscriptionName' | Set-AzContext -Name 'MyContextName'
```

<span data-ttu-id="313ae-136">In alternativa, specificare il nome o l'ID della sottoscrizione oppure l'ID tenant, se necessario:</span><span class="sxs-lookup"><span data-stu-id="313ae-136">Or give the subscription name or ID and the tenant ID if necessary:</span></span>

```azurepowershell-interactive
Set-AzContext -Name 'MyContextName' -Subscription 'MySubscriptionName' -Tenant '.......'
```

<span data-ttu-id="313ae-137">Se l'argomento `-Name` viene omesso, per il nome del contesto vengono usati il nome e l'ID della sottoscrizione, nel formato `Subscription Name (subscription-id)`.</span><span class="sxs-lookup"><span data-stu-id="313ae-137">If the `-Name` argument is omitted, then the subscription's name and ID are used as the context name in the format `Subscription Name (subscription-id)`.</span></span>

## <a name="change-the-active-azure-context"></a><span data-ttu-id="313ae-138">Cambiare il contesto di Azure attivo</span><span class="sxs-lookup"><span data-stu-id="313ae-138">Change the active Azure context</span></span>

<span data-ttu-id="313ae-139">Per cambiare il contesto di Azure attivo, è possibile usare sia `Set-AzContext` sia [Select-AzContext](/powershell/module/az.accounts/set-azcontext).</span><span class="sxs-lookup"><span data-stu-id="313ae-139">Both `Set-AzContext` and [Select-AzContext](/powershell/module/az.accounts/set-azcontext) can be used to change the active Azure context.</span></span> <span data-ttu-id="313ae-140">Come descritto nella sezione [Creare un nuovo contesto di Azure](#create-a-new-azure-context-from-subscription-information), `Set-AzContext` crea un nuovo contesto di Azure per una sottoscrizione, se non ne esiste già uno, e quindi imposta tale contesto come quello attivo.</span><span class="sxs-lookup"><span data-stu-id="313ae-140">As described in [Create a new Azure context](#create-a-new-azure-context-from-subscription-information), `Set-AzContext` creates a new Azure context for a subscription if one doesn't exist, and then switches to use that context as the active one.</span></span>

<span data-ttu-id="313ae-141">`Select-AzContext` deve essere usato solo con i contesti di Azure esistenti e funziona in modo simile all'uso di `Set-AzContext -Context`, ma è destinato all'uso con le pipeline:</span><span class="sxs-lookup"><span data-stu-id="313ae-141">`Select-AzContext` is meant to be used with existing Azure contexts only and works similarly to using `Set-AzContext -Context`, but is designed for use with piping:</span></span>

```azurepowershell-interactive
Set-AzContext -Context $(Get-AzContext -Name "mycontext") # Set a context with an inline Azure context object
Get-AzContext -Name "mycontext" | Select-AzContext # Set a context with a piped Azure context object
```

<span data-ttu-id="313ae-142">Analogamente a molti altri comandi di gestione di account e contesti disponibili in Azure PowerShell, `Set-AzContext` e `Select-AzContext` supportano l'argomento `-Scope`, quindi è possibile controllare il periodo di tempo in cui il contesto è attivo.</span><span class="sxs-lookup"><span data-stu-id="313ae-142">Like many other account and context management commands in Azure PowerShell, `Set-AzContext` and `Select-AzContext` support the `-Scope` argument so that you can control how long the context is active.</span></span> <span data-ttu-id="313ae-143">`-Scope` consente di cambiare il contesto attivo di una singola sessione senza cambiare l'impostazione predefinita:</span><span class="sxs-lookup"><span data-stu-id="313ae-143">`-Scope` lets you change a single session's active context without changing the default:</span></span>

```azurepowershell-interactive
Get-AzContext -Name "mycontext" | Select-AzContext -Scope Process
```

<span data-ttu-id="313ae-144">Per evitare di cambiare contesto per un'intera sessione di PowerShell, tutti i comandi di Azure PowerShell possono essere eseguiti in uno specifico contesto con l'argomento `-AzContext`:</span><span class="sxs-lookup"><span data-stu-id="313ae-144">To avoid switching contexts for a whole PowerShell session, all Azure PowerShell commands can be run against a given context with the `-AzContext` argument:</span></span>

```azurepowershell-interactive
$context = Get-AzContext -Name "mycontext"
New-AzVM -Name ExampleVM -AzContext $context
```

<span data-ttu-id="313ae-145">L'altro uso principale dei contesti con i cmdlet di Azure PowerShell consiste nell'esecuzione di comandi in background.</span><span class="sxs-lookup"><span data-stu-id="313ae-145">The other main use of contexts with Azure PowerShell cmdlets is to run background commands.</span></span> <span data-ttu-id="313ae-146">Per altre informazioni sull'esecuzione di processi di PowerShell con Azure PowerShell, vedere [Eseguire i cmdlet di Azure PowerShell nei processi di PowerShell](using-psjobs.md).</span><span class="sxs-lookup"><span data-stu-id="313ae-146">To learn more about running PowerShell Jobs using Azure PowerShell, see [Run Azure PowerShell cmdlets in PowerShell Jobs](using-psjobs.md).</span></span>

## <a name="save-azure-contexts-across-powershell-sessions"></a><span data-ttu-id="313ae-147">Salvare i contesti di Azure tra sessioni di PowerShell</span><span class="sxs-lookup"><span data-stu-id="313ae-147">Save Azure contexts across PowerShell sessions</span></span>

<span data-ttu-id="313ae-148">Per impostazione predefinita, i contesti di Azure vengono salvati per l'uso tra sessioni di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="313ae-148">By default, Azure contexts are saved for use between PowerShell sessions.</span></span> <span data-ttu-id="313ae-149">È possibile cambiare questo comportamento nei modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="313ae-149">You change this behavior in the following ways:</span></span>

* <span data-ttu-id="313ae-150">Accedere usando `-Scope Process` con `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="313ae-150">Sign in using `-Scope Process` with `Connect-AzAccount`.</span></span>

  ```azurepowershell
  Connect-AzAccount -Scope Process
  ```

  <span data-ttu-id="313ae-151">Il contesto di Azure restituito come parte di questo accesso è valido _solo_ per la sessione corrente e non verrà salvato automaticamente, indipendentemente dall'impostazione di salvataggio automatico dei contesti di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="313ae-151">The Azure context returned as part of this sign in is valid for the current session _only_ and will not be automatically saved, regardless of the Azure PowerShell context autosave setting.</span></span>
* <span data-ttu-id="313ae-152">Disabilitare il salvataggio automatico dei contesti di Azure PowerShell con il cmdlet [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave).</span><span class="sxs-lookup"><span data-stu-id="313ae-152">Disable AzurePowershell's context autosave with the [Disable-AzContextAutosave](/powershell/module/az.accounts/disable-azcontextautosave) cmdlet.</span></span>
  <span data-ttu-id="313ae-153">La disabilitazione del salvataggio automatico __non__ comporta la cancellazione di eventuali token archiviati.</span><span class="sxs-lookup"><span data-stu-id="313ae-153">Disabling context autosave __doesn't__ clear any stored tokens.</span></span> <span data-ttu-id="313ae-154">Per informazioni su come cancellare le informazioni dei contesti di Azure, vedere [Rimuovere contesti e credenziali di Azure](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="313ae-154">To learn how to clear stored Azure context information, see [Remove Azure contexts and credentials](#remove-azure-contexts-and-stored-credentials).</span></span>
* <span data-ttu-id="313ae-155">L'abilitazione esplicita del salvataggio automatico dei contesti di Azure può essere impostata con il cmdlet [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave).</span><span class="sxs-lookup"><span data-stu-id="313ae-155">Explicitly enable Azure context autosave can be enabled with the [Enable-AzContextAutosave](/powershell/module/az.accounts/enable-azcontextautosave) cmdlet.</span></span> <span data-ttu-id="313ae-156">Con il salvataggio automatico abilitato, tutti i contesti dell'utente vengono archiviati in locale per sessioni di PowerShell successive.</span><span class="sxs-lookup"><span data-stu-id="313ae-156">With autosave enabled, all of a user's contexts are stored locally for later PowerShell sessions.</span></span>
* <span data-ttu-id="313ae-157">Salvare manualmente i contesti con [Save-AzContext](/powershell/module/az.accounts/save-azcontext) per usarli in future sessioni di PowerShell, dove possono essere caricati con [Import-AzContext](/powershell/module/az.accounts/import-azcontext):</span><span class="sxs-lookup"><span data-stu-id="313ae-157">Manually save contexts with [Save-AzContext](/powershell/module/az.accounts/save-azcontext) to be used in future PowerShell sessions, where they can be loaded with [Import-AzContext](/powershell/module/az.accounts/import-azcontext):</span></span>

  ```azurepowershell
  Save-AzContext -Path current-context.json # Save the current context
  Save-AzContext -Profile $profileObject -Path other-context.json # Save a context object
  Import-AzContext -Path other-context.json # Load the context from a file and set it to the current context
  ```

> [!WARNING]
> <span data-ttu-id="313ae-158">La disabilitazione del salvataggio automatico dei contesti __non__ comporta la cancellazione delle informazioni salvate dei contesti archiviati.</span><span class="sxs-lookup"><span data-stu-id="313ae-158">Disabling context autosave __doesn't__ clear any stored context information that was saved.</span></span> <span data-ttu-id="313ae-159">Per rimuovere le informazioni archiviate, usare il cmdlet [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span><span class="sxs-lookup"><span data-stu-id="313ae-159">To remove stored information, use the [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext) cmdlet.</span></span> <span data-ttu-id="313ae-160">Per altre informazioni sulla rimozione dei contesti salvati, vedere [Rimuovere contesti e credenziali](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="313ae-160">For more on removing saved contexts, see [Remove contexts and credentials](#remove-azure-contexts-and-stored-credentials).</span></span>

<span data-ttu-id="313ae-161">Ognuno di questi comandi supporta il parametro `-Scope`, che accetta un valore `Process` per applicarlo solo al processo corrente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="313ae-161">Each of these commands supports the `-Scope` parameter, which can take a value of `Process` to only apply to the current running process.</span></span> <span data-ttu-id="313ae-162">Ad esempio, per assicurarsi che i contesti appena creati non vengano salvati dopo l'uscita da una sessione di PowerShell:</span><span class="sxs-lookup"><span data-stu-id="313ae-162">For example, to ensure that newly created contexts aren't saved after exiting a PowerShell session:</span></span>

```azurepowershell-interactive
Disable-AzContextAutosave -Scope Process
$context2 = Set-AzContext -Subscription "sub-id" -Tenant "other-tenant"
```

<span data-ttu-id="313ae-163">Le informazioni dei contesti e i token vengono archiviati nella directory `$env:USERPROFILE\.Azure` in Windows e in `$HOME/.Azure` in altre piattaforme.</span><span class="sxs-lookup"><span data-stu-id="313ae-163">Context information and tokens are stored in the `$env:USERPROFILE\.Azure` directory on Windows, and on `$HOME/.Azure` on other platforms.</span></span> <span data-ttu-id="313ae-164">Le informazioni sensibili, come gli ID sottoscrizione e gli ID tenant, possono essere comunque esposte nelle informazioni archiviate, tramite log o contesti salvati.</span><span class="sxs-lookup"><span data-stu-id="313ae-164">Sensitive information such as subscription IDs and tenant IDs may still be exposed in stored information, through logs or saved contexts.</span></span> <span data-ttu-id="313ae-165">Per informazioni su come cancellare le informazioni archiviate, vedere la sezione [Rimuovere contesti e credenziali](#remove-azure-contexts-and-stored-credentials).</span><span class="sxs-lookup"><span data-stu-id="313ae-165">To learn how to clear stored information, see the [Remove contexts and credentials](#remove-azure-contexts-and-stored-credentials) section.</span></span>

## <a name="remove-azure-contexts-and-stored-credentials"></a><span data-ttu-id="313ae-166">Rimuovere contesti e credenziali archiviate di Azure</span><span class="sxs-lookup"><span data-stu-id="313ae-166">Remove Azure contexts and stored credentials</span></span>

<span data-ttu-id="313ae-167">Per cancellare contesti e credenziali di Azure:</span><span class="sxs-lookup"><span data-stu-id="313ae-167">To clear Azure contexts and credentials:</span></span>

* <span data-ttu-id="313ae-168">Disconnettersi da un account con [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).</span><span class="sxs-lookup"><span data-stu-id="313ae-168">Sign out of an account with [Disconnect-AzAccount](/powershell/module/az.accounts/disconnect-azaccount).</span></span>
  <span data-ttu-id="313ae-169">È possibile disconnettersi da qualsiasi account in base ad account o contesto:</span><span class="sxs-lookup"><span data-stu-id="313ae-169">You can sign out of any account either by account or context:</span></span>

  ```azurepowershell-interactive
  Disconnect-AzAccount # Disconnect active account
  Disconnect-AzAccount -Username "user@contoso.com" # Disconnect by account name

  Disconnect-AzAccount -ContextName "subscription2" # Disconnect by context name
  Disconnect-AzAccount -AzureContext $contextObject # Disconnect using context object information
  ```

  <span data-ttu-id="313ae-170">Con la disconnessione vengono sempre rimossi i token di autenticazione e vengono cancellati i contesti salvati associati all'utente o al contesto disconnesso.</span><span class="sxs-lookup"><span data-stu-id="313ae-170">Disconnecting always removes stored authentication tokens and clears saved contexts associated with the disconnected user or context.</span></span>
* <span data-ttu-id="313ae-171">Usare [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span><span class="sxs-lookup"><span data-stu-id="313ae-171">Use [Clear-AzContext](/powershell/module/az.accounts/Clear-AzContext).</span></span> <span data-ttu-id="313ae-172">Questo cmdlet è garantito per rimuovere sempre i contesti e i token di autenticazione archiviati e consente anche di disconnettersi.</span><span class="sxs-lookup"><span data-stu-id="313ae-172">This cmdlet is guaranteed to always remove stored contexts and authentication tokens, and will also sign you out.</span></span>
* <span data-ttu-id="313ae-173">Rimuovere un contesto con [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):</span><span class="sxs-lookup"><span data-stu-id="313ae-173">Remove a context with [Remove-AzContext](/powershell/module/az.accounts/remove-azcontext):</span></span>

  ```azurepowershell-interactive
  Remove-AzContext -Name "mycontext" # Remove by name
  Get-AzContext -Name "mycontext" | Remove-AzContext # Remove by piping Azure context object
  ```

  <span data-ttu-id="313ae-174">Se si rimuove il contesto attivo, si verrà disconnessi da Azure e sarà necessario ripetere l'autenticazione con `Connect-AzAccount`.</span><span class="sxs-lookup"><span data-stu-id="313ae-174">If you remove the active context, you will be disconnected from Azure and need to reauthenticate with `Connect-AzAccount`.</span></span>

## <a name="see-also"></a><span data-ttu-id="313ae-175">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="313ae-175">See also</span></span>

* [<span data-ttu-id="313ae-176">Eseguire i cmdlet di Azure PowerShell nei processi di PowerShell</span><span class="sxs-lookup"><span data-stu-id="313ae-176">Run Azure PowerShell cmdlets in PowerShell Jobs</span></span>](using-psjobs.md)
* [<span data-ttu-id="313ae-177">Terminologia di Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="313ae-177">Azure Active Directory Terminology</span></span>](/azure/active-directory/fundamentals/active-directory-whatis#terminology)
* [<span data-ttu-id="313ae-178">Informazioni di riferimento su Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="313ae-178">Az.Accounts reference</span></span>](/powershell/module/az.accounts)
