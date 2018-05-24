---
title: Persistenza degli accessi utente tra le sessioni di PowerShell
description: Questo articolo illustra le nuove funzionalità di Azure PowerShell che consentono di riusare le credenziali e le altre informazioni utente in più sessioni di PowerShell.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/31/2017
ms.openlocfilehash: e60bc8d2ea5d30368b8cca3cc36e2fc949017574
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/23/2018
---
# <a name="persisting-user-logins-across-powershell-sessions"></a><span data-ttu-id="6a619-103">Persistenza degli accessi utente tra le sessioni di PowerShell</span><span class="sxs-lookup"><span data-stu-id="6a619-103">Persisting user logins across PowerShell sessions</span></span>

<span data-ttu-id="6a619-104">Nella versione di settembre 2017 di Azure PowerShell, i cmdlet di Azure Resource Manager introducono una nuova funzionalità di **salvataggio automatico del contesto Azure**,</span><span class="sxs-lookup"><span data-stu-id="6a619-104">In the September 2017 release of Azure PowerShell, Azure Resource Manager cmdlets introduce a new feature, **Azure Context Autosave**.</span></span> <span data-ttu-id="6a619-105">che supporta diversi nuovi scenari utente, tra cui:</span><span class="sxs-lookup"><span data-stu-id="6a619-105">This feature enables several new user scenarios, including:</span></span>

- <span data-ttu-id="6a619-106">Conservazione delle informazioni di accesso per il riutilizzo in nuove sessioni di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6a619-106">Retention of login information for reuse in new PowerShell sessions.</span></span>
- <span data-ttu-id="6a619-107">Uso semplificato di attività in background per eseguire cmdlet con esecuzione prolungata.</span><span class="sxs-lookup"><span data-stu-id="6a619-107">Easier use of background tasks for executing long-running cmdlets.</span></span>
- <span data-ttu-id="6a619-108">Passaggio da un account, una sottoscrizione o un ambiente all'altro senza un accesso separato.</span><span class="sxs-lookup"><span data-stu-id="6a619-108">Switch between accounts, subscriptions, and environments without a separate login.</span></span>
- <span data-ttu-id="6a619-109">Esecuzione simultanea di attività con credenziali e sottoscrizioni diverse dalla stessa sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6a619-109">Execution of tasks using different credentials and subscriptions, simultaneously, from the same PowerShell session.</span></span>

## <a name="azure-contexts-defined"></a><span data-ttu-id="6a619-110">Definizione dei contesti Azure</span><span class="sxs-lookup"><span data-stu-id="6a619-110">Azure contexts defined</span></span>

<span data-ttu-id="6a619-111">Un *contesto Azure* è un set di informazioni che definisce la destinazione dei cmdlet di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6a619-111">An *Azure context* is a set of information that defines the target of Azure PowerShell cmdlets.</span></span> <span data-ttu-id="6a619-112">Il contesto è costituito da cinque parti.</span><span class="sxs-lookup"><span data-stu-id="6a619-112">The context consists of five parts:</span></span>

- <span data-ttu-id="6a619-113">*Account*: entità servizio o nome utente usato per l'autenticazione delle comunicazioni con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a619-113">An *Account* - the UserName or Service Principal used to authenticate communications with Azure</span></span>
- <span data-ttu-id="6a619-114">*Sottoscrizione*: sottoscrizione di Azure contenente le risorse su cui vengono eseguire le operazioni.</span><span class="sxs-lookup"><span data-stu-id="6a619-114">A *Subscription* - The Azure Subscription containing the Resources being acted upon.</span></span>
- <span data-ttu-id="6a619-115">*Tenant*: tenant di Azure Active Directory contenente la sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="6a619-115">A *Tenant* - The Azure Active Directory tenant that contains your subscription.</span></span> <span data-ttu-id="6a619-116">I tenant sono particolarmente importanti per l'autenticazione di entità servizio.</span><span class="sxs-lookup"><span data-stu-id="6a619-116">Tenants are more important to ServicePrincipal authentication.</span></span>
- <span data-ttu-id="6a619-117">*Ambiente*: specifico cloud di Azure di destinazione, in genere il cloud globale di Azure.</span><span class="sxs-lookup"><span data-stu-id="6a619-117">An *Environment* - The particular Azure Cloud being targeted, usually the Azure global Cloud.</span></span>
  <span data-ttu-id="6a619-118">L'impostazione dell'ambiente consente tuttavia di specificare come destinazione anche cloud nazionali, per enti pubblici e locali (Azure Stack).</span><span class="sxs-lookup"><span data-stu-id="6a619-118">However, the environment setting allows you to target National, Government, and on-premises (Azure Stack) clouds as well.</span></span>
- <span data-ttu-id="6a619-119">*Credenziali*: informazioni usate da Azure per verificare l'identità dell'utente e la relativa autorizzazione ad accedere alle risorse in Azure.</span><span class="sxs-lookup"><span data-stu-id="6a619-119">*Credentials* - The information used by Azure to verify your identity and ensure your authorization to access resources in Azure</span></span>

<span data-ttu-id="6a619-120">Nelle versioni precedenti, il contesto Azure deve essere creato ogni volta che viene aperta una nuova sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6a619-120">In previous releases, your Azure Context had to be created each time you opened a new PowerShell session.</span></span> <span data-ttu-id="6a619-121">A partire da Azure PowerShell v4.4.0, è possibile abilitare il salvataggio automatico dei contesti Azure e il relativo riutilizzo all'apertura di una nuova sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6a619-121">Beginning with Azure PowerShell v4.4.0, you can enable the automatic saving and reuse of Azure Contexts whenever you open a new PowerShell session.</span></span>

## <a name="automatically-saving-the-context-for-the-next-login"></a><span data-ttu-id="6a619-122">Salvataggio automatico del contesto per l'accesso successivo</span><span class="sxs-lookup"><span data-stu-id="6a619-122">Automatically saving the context for the next login</span></span>

<span data-ttu-id="6a619-123">Per impostazione predefinita, Azure PowerShell rimuove le informazioni di contesto alla chiusura della sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6a619-123">By default, Azure PowerShell discards your context information whenever you close the PowerShell session.</span></span>

<span data-ttu-id="6a619-124">Per consentire ad Azure PowerShell di mantenere il contesto memorizzato dopo la chiusura della sessione di PowerShell, usare `Enable-AzureRmContextAutosave`.</span><span class="sxs-lookup"><span data-stu-id="6a619-124">To allow Azure PowerShell to remember your context after the PowerShell session is closed, use `Enable-AzureRmContextAutosave`.</span></span> <span data-ttu-id="6a619-125">Le informazioni relative al contesto e alle credenziali vengono salvate automaticamente in una speciale cartella nascosta nella directory dell'utente (`%AppData%\Roaming\Windows Azure PowerShell`).</span><span class="sxs-lookup"><span data-stu-id="6a619-125">Context and credential information are automatically saved in a special hidden folder in your user directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span>
<span data-ttu-id="6a619-126">Successivamente, ogni nuova sessione di PowerShell avrà come destinazione il contesto usato nell'ultima sessione.</span><span class="sxs-lookup"><span data-stu-id="6a619-126">Subsequently, each new PowerShell session targets the context used in your last session.</span></span>

<span data-ttu-id="6a619-127">Per annullare la memorizzazione del contesto e delle credenziali in PowerShell, usare `Disable-AzureRmContextAutoSave`.</span><span class="sxs-lookup"><span data-stu-id="6a619-127">To set PowerShell to forget your context and credentials, use `Disable-AzureRmContextAutoSave`.</span></span> <span data-ttu-id="6a619-128">Sarà necessario eseguire l'accesso ad Azure ogni volta che si apre una sessione di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6a619-128">You will need to log in to Azure every time you open a PowerShell session.</span></span>

<span data-ttu-id="6a619-129">I cmdlet che consentono di gestire i contesti Azure permettono anche un controllo con granularità fine.</span><span class="sxs-lookup"><span data-stu-id="6a619-129">The cmdlets that allow you to manage Azure contexts also allow you fine grained control.</span></span> <span data-ttu-id="6a619-130">Se si vuole, è possibile applicare le modifiche solo alla sessione di PowerShell corrente (ambito `Process`) o a ogni sessione di PowerShell (ambito `CurrentUser`).</span><span class="sxs-lookup"><span data-stu-id="6a619-130">If you want changes to apply only to the current PowerShell session (`Process` scope) or every PowerShell session (`CurrentUser` scope).</span></span> <span data-ttu-id="6a619-131">Questo opzioni sono descritte più dettagliatamente in [Uso degli ambiti dei contesti](#Using-Context-Scopes).</span><span class="sxs-lookup"><span data-stu-id="6a619-131">These options are discussed in mode detail in [Using Context Scopes](#Using-Context-Scopes).</span></span>

## <a name="running-azure-powershell-cmdlets-as-background-jobs"></a><span data-ttu-id="6a619-132">Esecuzione dei cmdlet di Azure PowerShell come processi in background</span><span class="sxs-lookup"><span data-stu-id="6a619-132">Running Azure PowerShell cmdlets as background jobs</span></span>

<span data-ttu-id="6a619-133">La funzionalità di **salvataggio automatico del contesto Azure** consente anche di condividere il contesto con processi in background di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6a619-133">The **Azure Context Autosave** feature also allows you to share you context with PowerShell background jobs.</span></span> <span data-ttu-id="6a619-134">In PowerShell è possibile avviare e monitorare attività con esecuzione prolungata come processi in background senza dover attendere il completamento delle attività.</span><span class="sxs-lookup"><span data-stu-id="6a619-134">PowerShell allows you to start and monitor long-executing tasks as background jobs without having to wait for the tasks to complete.</span></span> <span data-ttu-id="6a619-135">Per condividere le credenziali con i processi in background sono disponibili due diversi modi:</span><span class="sxs-lookup"><span data-stu-id="6a619-135">You can share credentials with background jobs in two different ways:</span></span>

- <span data-ttu-id="6a619-136">Passaggio del contesto come argomento</span><span class="sxs-lookup"><span data-stu-id="6a619-136">Passing the context as an argument</span></span>

  <span data-ttu-id="6a619-137">La maggior parte dei cmdlet di AzureRM consente di passare il contesto come parametro al cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a619-137">Most AzureRM cmdlets allow you to pass the context as a parameter to the cmdlet.</span></span> <span data-ttu-id="6a619-138">È possibile passare un contesto a un processo in background come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="6a619-138">You can pass a context to a background job as shown in the following example:</span></span>

  ```powershell
  PS C:\> $job = Start-Job { param ($ctx) New-AzureRmVm -AzureRmContext $ctx [... Additional parameters ...]} -ArgumentList (Get-AzureRmContext)
  ```

- <span data-ttu-id="6a619-139">Uso del contesto predefinito con il salvataggio automatico abilitato</span><span class="sxs-lookup"><span data-stu-id="6a619-139">Using the default context with Autosave enabled</span></span>

  <span data-ttu-id="6a619-140">Se si è abilitato il **salvataggio automatico del contesto**, i processi in background usano automaticamente il contesto salvato predefinito.</span><span class="sxs-lookup"><span data-stu-id="6a619-140">If you have enabled **Context Autosave**, background jobs automatically use the default saved context.</span></span>

  ```powershell
  PS C:\> $job = Start-Job { New-AzureRmVm [... Additional parameters ...]}
  ```

<span data-ttu-id="6a619-141">Quando è necessario conoscere il risultato dell'attività in background, usare `Get-Job` per controllare lo stato del processo e `Wait-Job` per attenderne il completamento.</span><span class="sxs-lookup"><span data-stu-id="6a619-141">When you need to know the outcome of the background task, use `Get-Job` to check the job status and `Wait-Job` to wait for the Job to complete.</span></span> <span data-ttu-id="6a619-142">Usare `Receive-Job` per acquisire o visualizzare l'output del processo in background.</span><span class="sxs-lookup"><span data-stu-id="6a619-142">Use `Receive-Job` to capture or display the output of the background job.</span></span> <span data-ttu-id="6a619-143">Per altre informazioni, vedere [About Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs) (Informazioni sui processi).</span><span class="sxs-lookup"><span data-stu-id="6a619-143">For more information, see [about_Jobs](/powershell/module/microsoft.powershell.core/about/about_jobs).</span></span>

## <a name="creating-selecting-renaming-and-removing-contexts"></a><span data-ttu-id="6a619-144">Creazione, selezione, ridenominazione e rimozione di contesti</span><span class="sxs-lookup"><span data-stu-id="6a619-144">Creating, selecting, renaming, and removing contexts</span></span>

<span data-ttu-id="6a619-145">Per creare un contesto, è necessario eseguire l'accesso ad Azure.</span><span class="sxs-lookup"><span data-stu-id="6a619-145">To create a context, you must be logged in to Azure.</span></span> <span data-ttu-id="6a619-146">Il cmdlet `Add-AzureRmAccount` (o il relativo alias `Login-AzureRmAccount`) imposta il contesto predefinito usato dai cmdlet di Azure PowerShell successivi e consente di accedere a qualsiasi sottoscrizione o tenant consentito dalle credenziali di accesso.</span><span class="sxs-lookup"><span data-stu-id="6a619-146">The `Add-AzureRmAccount` cmdlet (or its alias, `Login-AzureRmAccount`) sets the default context used by subsequent Azure PowerShell cmdlets, and allows you to access any tenants or subscriptions allowed by your login credentials.</span></span>

<span data-ttu-id="6a619-147">Per aggiungere un nuovo contesto dopo l'accesso, usare `Set-AzureRmContext` o il relativo alias `Select-AzureRmSubscription`.</span><span class="sxs-lookup"><span data-stu-id="6a619-147">To add a new context after login, use `Set-AzureRmContext` (or its alias, `Select-AzureRmSubscription`).</span></span>

```powershell
PS C:\> Set-AzureRMContext -Subscription "Contoso Subscription 1" -Name "Contoso1"
```

<span data-ttu-id="6a619-148">L'esempio precedente aggiunge un nuovo contesto specificando come destinazione "Contoso Subscription 1" con le credenziali correnti.</span><span class="sxs-lookup"><span data-stu-id="6a619-148">The previous example adds a new context targeting 'Contoso Subscription 1' using your current credentials.</span></span> <span data-ttu-id="6a619-149">Il nuovo contesto è denominato "Contoso1".</span><span class="sxs-lookup"><span data-stu-id="6a619-149">The new context is named 'Contoso1'.</span></span> <span data-ttu-id="6a619-150">Se non si specifica un nome per il contesto, verrà usato un nome predefinito contenente l'ID account e l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="6a619-150">If you do not provide a name for the context, a default name, using the account ID and subscription ID is used.</span></span>

<span data-ttu-id="6a619-151">Per rinominare un contesto esistente, usare il cmdlet `Rename-AzureRmContext`,</span><span class="sxs-lookup"><span data-stu-id="6a619-151">To rename an existing context, use the `Rename-AzureRmContext` cmdlet.</span></span> <span data-ttu-id="6a619-152">Ad esempio: </span><span class="sxs-lookup"><span data-stu-id="6a619-152">For example:</span></span>

```powershell
PS C:\> Rename-AzureRmContext '[user1@contoso.org; 123456-7890-1234-564321]` 'Contoso2'
```

<span data-ttu-id="6a619-153">Questo esempio rinomina il contesto denominato automaticamente `[user1@contoso.org; 123456-7890-1234-564321]` con il semplice nome "Contoso2".</span><span class="sxs-lookup"><span data-stu-id="6a619-153">This example renames the context with automatic name `[user1@contoso.org; 123456-7890-1234-564321]` to the simple name 'Contoso2'.</span></span> <span data-ttu-id="6a619-154">I cmdlet che gestiscono i contesti usano anche il completamento tramite tasto TAB, consentendo così di selezionare rapidamente il contesto.</span><span class="sxs-lookup"><span data-stu-id="6a619-154">Cmdlets that manage contexts also use tab completion, allowing you to quickly select the context.</span></span>

<span data-ttu-id="6a619-155">Infine, per rimuovere un contesto usare il cmdlet `Remove-AzureRmContext`,</span><span class="sxs-lookup"><span data-stu-id="6a619-155">Finally, to remove a context, use the `Remove-AzureRmContext` cmdlet.</span></span>  <span data-ttu-id="6a619-156">Ad esempio: </span><span class="sxs-lookup"><span data-stu-id="6a619-156">For example:</span></span>

```powershell
PS C:\> Remove-AzureRmContext Contoso2
```

<span data-ttu-id="6a619-157">Questo esempio annulla la memorizzazione del contesto denominato "Contoso2".</span><span class="sxs-lookup"><span data-stu-id="6a619-157">Forgets the context that was named 'Contoso2'.</span></span> <span data-ttu-id="6a619-158">È possibile ricreare questo contesto in seguito usando `Set-AzureRmContext`</span><span class="sxs-lookup"><span data-stu-id="6a619-158">You can recreate this context subsequently using `Set-AzureRmContext`</span></span>

## <a name="removing-credentials"></a><span data-ttu-id="6a619-159">Rimozione delle credenziali</span><span class="sxs-lookup"><span data-stu-id="6a619-159">Removing credentials</span></span>

<span data-ttu-id="6a619-160">È possibile rimuovere tutte le credenziali e i contesti associati per un utente o un'entità servizio usando `Remove-AzureRmAccount` (denominato anche `Logout-AzureRmAccount`).</span><span class="sxs-lookup"><span data-stu-id="6a619-160">You can remove all credentials and associated contexts for a user or service principal using `Remove-AzureRmAccount` (also known as `Logout-AzureRmAccount`).</span></span> <span data-ttu-id="6a619-161">Se eseguito senza parametri, il cmdlet `Remove-AzureRmAccount` rimuove tutte le credenziali e i contesti associati all'utente o all'entità servizio nel contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="6a619-161">When executed without parameters, the `Remove-AzureRmAccount` cmdlet removes all credentials and contexts associated with the User or Service Principal in the current context.</span></span> <span data-ttu-id="6a619-162">È possibile passare un nome utente, un nome di entità servizio o un contesto per specificare come destinazione una determinata entità di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="6a619-162">You may pass in a Username, Service Principal Name, or context to target a particular principal.</span></span>

```powershell
Remove-AzureRmAccount user1@contoso.org
```

## <a name="using-context-scopes"></a><span data-ttu-id="6a619-163">Uso degli ambiti dei contesti</span><span class="sxs-lookup"><span data-stu-id="6a619-163">Using context scopes</span></span>

<span data-ttu-id="6a619-164">In alcuni casi può essere opportuno selezionare, modificare o rimuovere un contesto in una sessione di PowerShell senza influire su altre sessioni.</span><span class="sxs-lookup"><span data-stu-id="6a619-164">Occasionally, you may want to select, change, or remove a context in a PowerShell session without impacting other sessions.</span></span> <span data-ttu-id="6a619-165">Per modificare il comportamento predefinito dei cmdlet per il contesto, usare il parametro `Scope`.</span><span class="sxs-lookup"><span data-stu-id="6a619-165">To change the default behavior of context cmdlets, use the `Scope` parameter.</span></span> <span data-ttu-id="6a619-166">L'ambito `Process` esegue l'override del comportamento predefinito determinando l'applicazione solo per la sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="6a619-166">The `Process` scope overrides the default behavior by making it apply only for the current session.</span></span> <span data-ttu-id="6a619-167">Al contrario, l'ambito `CurrentUser` modifica il contesto in tutte le sessioni, anziché solo nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="6a619-167">Conversely `CurrentUser` scope changes the context in all sessions, instead of just the current session.</span></span>

<span data-ttu-id="6a619-168">Ad esempio, per modificare il contesto predefinito nella sessione di PowerShell corrente senza influire sulle altre finestre o sul contesto usato alla successiva apertura di una sessione, usare:</span><span class="sxs-lookup"><span data-stu-id="6a619-168">As an example, to change the default context in the current PowerShell session without impacting other windows, or the context used the next time a session is opened, use:</span></span>

```powershell
PS C:\> Select-AzureRmContext Contoso1 -Scope Process
```

## <a name="how-the-context-autosave-setting-is-remembered"></a><span data-ttu-id="6a619-169">Memorizzazione dell'impostazione di salvataggio automatico del contesto</span><span class="sxs-lookup"><span data-stu-id="6a619-169">How the context autosave setting is remembered</span></span>

<span data-ttu-id="6a619-170">L'impostazione di salvataggio automatico del contesto viene salvata nella directory di Azure PowerShell dell'utente (`%AppData%\Roaming\Windows Azure PowerShell`).</span><span class="sxs-lookup"><span data-stu-id="6a619-170">The context AutoSave setting is saved to the user Azure PowerShell directory (`%AppData%\Roaming\Windows Azure PowerShell`).</span></span> <span data-ttu-id="6a619-171">Alcune tipologie di account computer potrebbero non avere accesso a tale directory.</span><span class="sxs-lookup"><span data-stu-id="6a619-171">Some kinds of computer accounts may not have access to this directory.</span></span> <span data-ttu-id="6a619-172">In tali scenari, è possibile usare la variabile di ambiente seguente:</span><span class="sxs-lookup"><span data-stu-id="6a619-172">For such scenarios, you can use the environment variable</span></span>

```powershell
$env:AzureRmContextAutoSave="true" | "false"
```

<span data-ttu-id="6a619-173">Se è impostata su "true", il contesto viene salvato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="6a619-173">If set to 'true', the context is automatically saved.</span></span> <span data-ttu-id="6a619-174">Se è impostata su "false", il contesto non viene salvato.</span><span class="sxs-lookup"><span data-stu-id="6a619-174">If set to 'false', the context is not saved.</span></span>

## <a name="changes-to-the-azurermprofile-module"></a><span data-ttu-id="6a619-175">Modifiche apportate al modulo AzureRM.Profile</span><span class="sxs-lookup"><span data-stu-id="6a619-175">Changes to the AzureRM.Profile module</span></span>

<span data-ttu-id="6a619-176">Nuovi cmdlet per la gestione del contesto</span><span class="sxs-lookup"><span data-stu-id="6a619-176">New cmdlets for managing context</span></span>

- <span data-ttu-id="6a619-177">[Enable-AzureRmContextAutosave][enable]: consente di salvare il contesto tra le sessioni di PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6a619-177">[Enable-AzureRmContextAutosave][enable] - Allow saving the context between powershell sessions.</span></span>
  <span data-ttu-id="6a619-178">Qualsiasi modifica viene applicata al contesto globale.</span><span class="sxs-lookup"><span data-stu-id="6a619-178">Any changes alter the global context.</span></span>
- <span data-ttu-id="6a619-179">[Disable-AzureRmContextAutosave][disable]: disattiva il salvataggio automatico del contesto.</span><span class="sxs-lookup"><span data-stu-id="6a619-179">[Disable-AzureRmContextAutosave][disable] - Turn off autosaving the context.</span></span> <span data-ttu-id="6a619-180">Per ogni nuova sessione di PowerShell è necessario ripetere l'accesso.</span><span class="sxs-lookup"><span data-stu-id="6a619-180">Each new PowerShell session is required to log in again.</span></span>
- <span data-ttu-id="6a619-181">[Select-AzureRmContext][select]: seleziona un contesto come predefinito.</span><span class="sxs-lookup"><span data-stu-id="6a619-181">[Select-AzureRmContext][select] - Select a context as the default.</span></span> <span data-ttu-id="6a619-182">Tutti i cmdlet successivi useranno le credenziali di questo contesto per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="6a619-182">All subsequent cmdlets use the credentials in this context for authentication.</span></span>
- <span data-ttu-id="6a619-183">[Remove-AzureRmAccount][remove-cred]: rimuove tutte le credenziali e i contesti associati a un account.</span><span class="sxs-lookup"><span data-stu-id="6a619-183">[Remove-AzureRmAccount][remove-cred] - Remove all credentials and contexts associated with an account.</span></span>
- <span data-ttu-id="6a619-184">[Remove-AzureRmContext][remove-context]: rimuove un contesto denominato.</span><span class="sxs-lookup"><span data-stu-id="6a619-184">[Remove-AzureRmContext][remove-context] - Remove a named context.</span></span>
- <span data-ttu-id="6a619-185">[Rename-AzureRmContext][rename]: rinomina un contesto esistente.</span><span class="sxs-lookup"><span data-stu-id="6a619-185">[Rename-AzureRmContext][rename] - Rename an existing context.</span></span>

<span data-ttu-id="6a619-186">Modifiche apportate ai cmdlet per i profili esistenti</span><span class="sxs-lookup"><span data-stu-id="6a619-186">Changes to existing profile cmdlets</span></span>

- <span data-ttu-id="6a619-187">[Add-AzureRmAccount][login]: consente di limitare l'ambito dell'accesso al processo o all'utente corrente,</span><span class="sxs-lookup"><span data-stu-id="6a619-187">[Add-AzureRmAccount][login] - Allow scoping of the login to the process or the current user.</span></span>
  <span data-ttu-id="6a619-188">nonché di denominare il contesto predefinito dopo l'accesso.</span><span class="sxs-lookup"><span data-stu-id="6a619-188">Allow naming the default context after login.</span></span>
- <span data-ttu-id="6a619-189">[Import-AzureRmContext][import]: consente di limitare l'ambito dell'accesso al processo o all'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="6a619-189">[Import-AzureRmContext][import] - Allow scoping of the login to the process or the current user.</span></span>
- <span data-ttu-id="6a619-190">[Set-AzureRmContext][set-context]: consente di selezionare contesti denominati esistenti e limitare l'ambito delle modifiche al processo o all'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="6a619-190">[Set-AzureRmContext][set-context] - Allow selection of existing named contexts, and scope changes to the process or current user.</span></span>

<!-- Hyperlinks -->
[enable]: /powershell/module/azurerm.profile/Enable-AzureRmContextAutosave
[disable]: /powershell/module/azurerm.profile/Disable-AzureRmContextAutosave
[select]: /powershell/module/azurerm.profile/Select-AzureRmContext
[remove-cred]: /powershell/module/azurerm.profile/Remove-AzureRmAccount
[remove-context]: /powershell/module/azurerm.profile/Remove-AzureRmContext
[rename]: /powershell/module/azurerm.profile/Rename-AzureRmContext

<!-- Updated cmdlets -->
[login]: /powershell/module/azurerm.profile/Add-AzureRmAccount
[import]: /powershell/module/azurerm.profile/Import-AzureRmAccount
[set-context]: /powershell/module/azurerm.profile/Import-AzureRmContext
