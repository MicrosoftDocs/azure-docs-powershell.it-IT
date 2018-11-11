---
title: Conservare le credenziali utente tra le sessioni di PowerShell
description: Informazioni su come riutilizzare le credenziali di Azure e altre informazioni in più sessioni di PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.openlocfilehash: a07b5fe8cd532f99038d7f0ce10b3b891c896da1
ms.sourcegitcommit: ac4b53bb42a25aae013a9d8cd9ae98ada9397274
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/08/2018
ms.locfileid: "51273940"
---
# <a name="persist-user-credentials-across-powershell-sessions"></a><span data-ttu-id="ad658-103">Conservare le credenziali utente tra le sessioni di PowerShell</span><span class="sxs-lookup"><span data-stu-id="ad658-103">Persist user credentials across PowerShell sessions</span></span>

<span data-ttu-id="ad658-104">Azure PowerShell offre una funzionalità denominata **salvataggio automatico del contesto Azure**, che fornisce le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="ad658-104">Azure PowerShell offers a feature called **Azure Context Autosave**, which gives the following features:</span></span>

- <span data-ttu-id="ad658-105">Conservazione delle informazioni di accesso per il riutilizzo in nuove sessioni di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ad658-105">Retention of sign-in information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="ad658-106">Uso semplificato di attività in background per eseguire cmdlet con esecuzione prolungata.</span><span class="sxs-lookup"><span data-stu-id="ad658-106">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="ad658-107">Passaggio da un account, una sottoscrizione o un ambiente all'altro senza un accesso separato.</span><span class="sxs-lookup"><span data-stu-id="ad658-107">Switch between accounts, subscriptions, and environments without a separate sign-in.</span></span>
- <span data-ttu-id="ad658-108">Esecuzione simultanea di attività con credenziali e sottoscrizioni diverse dalla stessa sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ad658-108">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="ad658-109">Definizione dei contesti Azure</span><span class="sxs-lookup"><span data-stu-id="ad658-109">Azure contexts defined</span></span>

<span data-ttu-id="ad658-110">Un *contesto Azure* è un set di informazioni che definisce la destinazione dei cmdlet di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ad658-110">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="ad658-111">Il contesto è costituito da cinque parti.</span><span class="sxs-lookup"><span data-stu-id="ad658-111">The context consists of five parts:</span></span>

- <span data-ttu-id="ad658-112">*Account*: entità servizio o nome utente usato per l'autenticazione delle comunicazioni con Azure.</span><span class="sxs-lookup"><span data-stu-id="ad658-112">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="ad658-113">*Sottoscrizione*: sottoscrizione di Azure con le risorse su cui vengono eseguite le operazioni.</span><span class="sxs-lookup"><span data-stu-id="ad658-113">A *Subscription* - The Azure Subscription with the Resources being acted upon.</span></span>
- <span data-ttu-id="ad658-114">*Tenant*: tenant di Azure Active Directory contenente la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ad658-114">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="ad658-115">I tenant sono particolarmente importanti per l'autenticazione di entità servizio.</span><span class="sxs-lookup"><span data-stu-id="ad658-115">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="ad658-116">*Ambiente*: specifico cloud di Azure di destinazione, in genere il cloud globale di Azure.</span><span class="sxs-lookup"><span data-stu-id="ad658-116">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="ad658-117">L'impostazione dell'ambiente consente tuttavia di specificare come destinazione anche cloud nazionali, per enti pubblici e locali (Azure Stack).</span><span class="sxs-lookup"><span data-stu-id="ad658-117">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="ad658-118">*Credenziali*: informazioni usate da Azure per verificare l'identità dell'utente e la relativa autorizzazione ad accedere alle risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="ad658-118">*Credentials* - The information used by Azure to verify your identity and confirm your authorization to access resources in Azure</span></span>

<span data-ttu-id="ad658-119">Nelle versioni precedenti deve essere creato un contesto Azure ogni volta che viene aperta una nuova sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ad658-119">In previous releases, an Azure Context had to be created each time you opened a new PowerShell session.</span></span> <span data-ttu-id="ad658-120">A partire da Azure PowerShell v4.4.0, i contesti Azure possono essere salvati automaticamente all'apertura di una nuova sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ad658-120">Beginning with Azure PowerShell v4.4.0, Azure Contexts can automatically be saved whenever opening a new PowerShell session.</span></span>

## <a name="automatically-save-the-context-for-the-next-sign-in"></a><span data-ttu-id="ad658-121">Salvare automaticamente il contesto per l'accesso successivo</span><span class="sxs-lookup"><span data-stu-id="ad658-121">Automatically save the context for the next sign-in</span></span>

<span data-ttu-id="ad658-122">Nella versione 6.3.0 e nelle successive, Azure PowerShell conserva automaticamente le informazioni del contesto tra le sessioni.</span><span class="sxs-lookup"><span data-stu-id="ad658-122">In versions 6.3.0 and later, Azure PowerShell retains your context information automatically between sessions.</span></span> <span data-ttu-id="ad658-123">Per annullare la memorizzazione del contesto e delle credenziali in PowerShell, usare `Disable-AzureRmContextAutoSave`.</span><span class="sxs-lookup"><span data-stu-id="ad658-123">To set PowerShell to forget your context and credentials, use `Disable-AzureRmContextAutoSave`.</span></span> <span data-ttu-id="ad658-124">Sarà necessario eseguire l'accesso ad Azure ogni volta che si apre una sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ad658-124">You'll need to sign in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="ad658-125">Per consentire ad Azure PowerShell di mantenere il contesto memorizzato dopo la chiusura della sessione di PowerShell, usare `Enable-AzureRmContextAutosave`.</span><span class="sxs-lookup"><span data-stu-id="ad658-125">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzureRmContextAutosave`.</span></span> <span data-ttu-id="ad658-126">Le informazioni relative al contesto e alle credenziali vengono salvate automaticamente in una speciale cartella nascosta nella directory dell'utente (`%AppData%\Roaming\Windows Azure PowerShell`).</span><span class="sxs-lookup"><span data-stu-id="ad658-126">Context and credential information are automatically saved in a special hidden folder in your user directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span>
<span data-ttu-id="ad658-127">Ogni nuova sessione di PowerShell avrà come destinazione il contesto usato nell'ultima sessione.</span><span class="sxs-lookup"><span data-stu-id="ad658-127">Each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="ad658-128">I cmdlet che consentono di gestire i contesti Azure permettono anche un controllo con granularità fine.</span><span class="sxs-lookup"><span data-stu-id="ad658-128">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="ad658-129">Se si vuole, è possibile applicare le modifiche solo alla sessione di PowerShell corrente (ambito `Process`) o a ogni sessione di PowerShell (ambito `CurrentUser`).</span><span class="sxs-lookup"><span data-stu-id="ad658-129">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="ad658-130">Questo opzioni sono descritte più dettagliatamente in [Uso degli ambiti dei contesti](#Using-Context-Scopes).</span><span class="sxs-lookup"><span data-stu-id="ad658-130">These options are discussed in mode detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="ad658-131">Esecuzione dei cmdlet di Azure PowerShell come processi in background</span><span class="sxs-lookup"><span data-stu-id="ad658-131">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="ad658-132">La funzionalità di **salvataggio automatico del contesto Azure** consente anche di condividere il contesto con processi in background di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ad658-132">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="ad658-133">In PowerShell è possibile avviare e monitorare attività con esecuzione prolungata come processi in background senza dover attendere il completamento delle attività.</span><span class="sxs-lookup"><span data-stu-id="ad658-133">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="ad658-134">Per condividere le credenziali con i processi in background sono disponibili due diversi modi:</span><span class="sxs-lookup"><span data-stu-id="ad658-134">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="ad658-135">Passaggio del contesto come argomento</span><span class="sxs-lookup"><span data-stu-id="ad658-135">Passing the context as an argument</span></span>

  <span data-ttu-id="ad658-136">La maggior parte dei cmdlet di AzureRM consente di passare il contesto come parametro al cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad658-136">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="ad658-137">È possibile passare un contesto a un processo in background come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="ad658-137">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- <span data-ttu-id="ad658-138">Uso del contesto predefinito con il salvataggio automatico abilitato</span><span class="sxs-lookup"><span data-stu-id="ad658-138">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="ad658-139">Se si è abilitato il **salvataggio automatico del contesto**, i processi in background usano automaticamente il contesto salvato predefinito.</span><span class="sxs-lookup"><span data-stu-id="ad658-139">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell-interactive
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

<span data-ttu-id="ad658-140">Quando è necessario conoscere il risultato dell'attività in background, usare `Get-Job` per controllare lo stato del processo e `Wait-Job` per attenderne il completamento.</span><span class="sxs-lookup"><span data-stu-id="ad658-140">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="ad658-141">Usare `Receive-Job` per acquisire o visualizzare l'output del processo in background.</span><span class="sxs-lookup"><span data-stu-id="ad658-141">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="ad658-142">Per altre informazioni, vedere [About Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs) (Informazioni sui processi).</span><span class="sxs-lookup"><span data-stu-id="ad658-142">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="ad658-143">Creazione, selezione, ridenominazione e rimozione di contesti</span><span class="sxs-lookup"><span data-stu-id="ad658-143">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="ad658-144">Per creare un contesto, è necessario eseguire l'accesso ad Azure.</span><span class="sxs-lookup"><span data-stu-id="ad658-144">To create a context, you must be signed in to Azure.</span></span> <span data-ttu-id="ad658-145">Il cmdlet `Connect-AzureRmAccount` (o il relativo alias `Login-AzureRmAccount`) imposta il contesto predefinito usato dai cmdlet di Azure PowerShell e consente di accedere a qualsiasi sottoscrizione o tenant consentito dalle credenziali.</span><span class="sxs-lookup"><span data-stu-id="ad658-145">The `Connect-AzureRmAccount` cmdlet (or its alias, `Login-AzureRmAccount`) sets the default context used by Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your credentials.</span></span>

<span data-ttu-id="ad658-146">Per aggiungere un nuovo contesto dopo l'accesso, usare `Set-AzureRmContext` o il relativo alias `Select-AzureRmSubscription`.</span><span class="sxs-lookup"><span data-stu-id="ad658-146">To add a new context after sign-in, use `Set-AzureRmContext` (or its alias, `Select-AzureRmSubscription`).</span></span>

```azurepowershell-interactive
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="ad658-147">L'esempio precedente aggiunge un nuovo contesto specificando come destinazione "Contoso Subscription 1" con le credenziali correnti.</span><span class="sxs-lookup"><span data-stu-id="ad658-147">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="ad658-148">Il nuovo contesto è denominato "Contoso1".</span><span class="sxs-lookup"><span data-stu-id="ad658-148">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="ad658-149">Se non si specifica un nome per il contesto, verrà usato un nome predefinito basato su l'ID account e l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ad658-149">If you don't provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="ad658-150">Per rinominare un contesto esistente, usare il cmdlet `Rename-AzureRmContext`,</span><span class="sxs-lookup"><span data-stu-id="ad658-150">To rename an existing context, use the `Rename-AzureRmContext` cmdlet.</span></span> <span data-ttu-id="ad658-151">Ad esempio: </span><span class="sxs-lookup"><span data-stu-id="ad658-151">For example:</span></span>

```azurepowershell-interactive
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="ad658-152">Questo esempio rinomina il contesto denominato automaticamente `[user1@contoso.org; 123456-7890-1234-564321]` con il semplice nome "Contoso2".</span><span class="sxs-lookup"><span data-stu-id="ad658-152">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="ad658-153">I cmdlet che gestiscono i contesti usano anche il completamento tramite tasto TAB, consentendo così di selezionare rapidamente il contesto.</span><span class="sxs-lookup"><span data-stu-id="ad658-153">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="ad658-154">Infine, per rimuovere un contesto usare il cmdlet `Remove-AzureRmContext`,</span><span class="sxs-lookup"><span data-stu-id="ad658-154">Finally, to remove a context, use the `Remove-AzureRmContext` cmdlet.</span></span>  <span data-ttu-id="ad658-155">Ad esempio: </span><span class="sxs-lookup"><span data-stu-id="ad658-155">For example:</span></span>

```azurepowershell-interactive
PS C:\> Remove-AzureRmContext Contoso2
```

<span data-ttu-id="ad658-156">Questo esempio annulla la memorizzazione del contesto denominato "Contoso2".</span><span class="sxs-lookup"><span data-stu-id="ad658-156">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="ad658-157">È possibile ricreare questo contesto usando `Set-AzureRmContext`</span><span class="sxs-lookup"><span data-stu-id="ad658-157">You can recreate this context using `Set-AzureRmContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="ad658-158">Rimozione delle credenziali</span><span class="sxs-lookup"><span data-stu-id="ad658-158">Removing credentials</span></span>

<span data-ttu-id="ad658-159">È possibile rimuovere tutte le credenziali e i contesti associati per un utente o un'entità servizio usando `Disconnect-AzureRmAccount` (denominato anche `Logout-AzureRmAccount`).</span><span class="sxs-lookup"><span data-stu-id="ad658-159">You can remove all credentials and associated contexts for a user or service principal using `Disconnect-AzureRmAccount` (also known as `Logout-AzureRmAccount`).</span></span> <span data-ttu-id="ad658-160">Se eseguito senza parametri, il cmdlet `Disconnect-AzureRmAccount` rimuove tutte le credenziali e i contesti associati all'utente o all'entità servizio nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="ad658-160">When executed without parameters, the `Disconnect-AzureRmAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="ad658-161">È possibile passare un nome utente, un nome di entità servizio o un contesto per specificare come destinazione una determinata entità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="ad658-161">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```azurepowershell-interactive
Disconnect-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="ad658-162">Uso degli ambiti dei contesti</span><span class="sxs-lookup"><span data-stu-id="ad658-162">Using context scopes</span></span>

<span data-ttu-id="ad658-163">In alcuni casi può essere opportuno selezionare, modificare o rimuovere un contesto in una sessione di PowerShell senza influire su altre sessioni.</span><span class="sxs-lookup"><span data-stu-id="ad658-163">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="ad658-164">Per modificare il comportamento predefinito dei cmdlet per il contesto, usare il parametro `Scope`.</span><span class="sxs-lookup"><span data-stu-id="ad658-164">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="ad658-165">L'ambito `Process` esegue l'override del comportamento predefinito determinando l'applicazione solo per la sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="ad658-165">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="ad658-166">Al contrario, l'ambito `CurrentUser` modifica il contesto in tutte le sessioni, anziché solo nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="ad658-166">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="ad658-167">Ad esempio, per modificare il contesto predefinito nella sessione di PowerShell corrente senza influire sulle altre finestre o sul contesto usato alla successiva apertura di una sessione, usare:</span><span class="sxs-lookup"><span data-stu-id="ad658-167">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```azurepowershell-interactive
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="ad658-168">Memorizzazione dell'impostazione di salvataggio automatico del contesto</span><span class="sxs-lookup"><span data-stu-id="ad658-168">How the context autosave setting is remembered</span></span>

<span data-ttu-id="ad658-169">L'impostazione di salvataggio automatico del contesto viene salvata nella directory di Azure PowerShell dell'utente (`%AppData%\Roaming\Windows Azure PowerShell`).</span><span class="sxs-lookup"><span data-stu-id="ad658-169">The context AutoSave setting is saved to the user Azure PowerShell directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span> <span data-ttu-id="ad658-170">Alcune tipologie di account computer potrebbero non avere accesso a tale directory.</span><span class="sxs-lookup"><span data-stu-id="ad658-170">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="ad658-171">In tali scenari, è possibile usare la variabile di ambiente seguente:</span><span class="sxs-lookup"><span data-stu-id="ad658-171">For such scenarios, you can use the environment variable</span></span>

```azurepowershell-interactive
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="ad658-172">Quando è impostata su "true", il contesto viene salvato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="ad658-172">When set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="ad658-173">Se è impostata su "false", il contesto non viene salvato.</span><span class="sxs-lookup"><span data-stu-id="ad658-173">If set to 'false', the context isn't saved.</span></span>

## <a name="changes-to-the-azurermprofile-module"></a><span data-ttu-id="ad658-174">Modifiche apportate al modulo AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="ad658-174">Changes to the AzureRM.Profile module</span></span>

<span data-ttu-id="ad658-175">Nuovi cmdlet per la gestione del contesto</span><span class="sxs-lookup"><span data-stu-id="ad658-175">New cmdlets for managing context</span></span>

- <span data-ttu-id="ad658-176">[Enable-AzureRmContextAutosave][enable]: consente di salvare il contesto tra le sessioni di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ad658-176">[Enable-AzureRmContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="ad658-177">Qualsiasi modifica viene applicata al contesto globale.</span><span class="sxs-lookup"><span data-stu-id="ad658-177">Any changes alter the global context.</span></span>
- <span data-ttu-id="ad658-178">[Disable-AzureRmContextAutosave][disable]: disattiva il salvataggio automatico del contesto.</span><span class="sxs-lookup"><span data-stu-id="ad658-178">[Disable-AzureRmContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="ad658-179">Per ogni nuova sessione di PowerShell è necessario ripetere l'accesso.</span><span class="sxs-lookup"><span data-stu-id="ad658-179">Each new PowerShell session is required to sign in again.</span></span>
- <span data-ttu-id="ad658-180">[Select-AzureRmContext][select]: seleziona un contesto come predefinito.</span><span class="sxs-lookup"><span data-stu-id="ad658-180">[Select-AzureRmContext][select] - Select a context as the default.</span></span> <span data-ttu-id="ad658-181">Tutti i cmdlet usano le credenziali in questo contesto per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="ad658-181">All cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="ad658-182">[Disconnect-AzureRmAccount][remove-cred]: rimuove tutte le credenziali e i contesti associati a un account.</span><span class="sxs-lookup"><span data-stu-id="ad658-182">[Disconnect-AzureRmAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="ad658-183">[Remove-AzureRmContext][remove-context]: rimuove un contesto denominato.</span><span class="sxs-lookup"><span data-stu-id="ad658-183">[Remove-AzureRmContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="ad658-184">[Rename-AzureRmContext][rename]: rinomina un contesto esistente.</span><span class="sxs-lookup"><span data-stu-id="ad658-184">[Rename-AzureRmContext][rename] - Rename an existing context.</span></span>

<span data-ttu-id="ad658-185">Modifiche apportate ai cmdlet per i profili esistenti</span><span class="sxs-lookup"><span data-stu-id="ad658-185">Changes to existing profile cmdlets</span></span>

- <span data-ttu-id="ad658-186">[Add-AzureRmAccount][login]: consente di limitare l'ambito dell'accesso al processo o all'utente corrente,</span><span class="sxs-lookup"><span data-stu-id="ad658-186">[Add-AzureRmAccount][login] - Allow scoping of the sign-in to the process or the current user.</span></span>
  <span data-ttu-id="ad658-187">nonché di denominare il contesto predefinito dopo l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="ad658-187">Allow naming the default context after authentication.</span></span>
- <span data-ttu-id="ad658-188">[Import-AzureRmContext][import]: consente di limitare l'ambito dell'accesso al processo o all'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="ad658-188">[Import-AzureRmContext][import] - Allow scoping of the sign-in to the process or the current user.</span></span>
- <span data-ttu-id="ad658-189">[Set-AzureRmContext][set-context]: consente di selezionare contesti denominati esistenti e limitare l'ambito delle modifiche al processo o all'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="ad658-189">[Set-AzureRmContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Disconnect-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Connect-AzureRmAccount
[import]:  /powershell/module/azurerm.profile/Import-AzureRmContext
[set-context]: /powershell/module/azurerm.profile/Set-AzureRmContext