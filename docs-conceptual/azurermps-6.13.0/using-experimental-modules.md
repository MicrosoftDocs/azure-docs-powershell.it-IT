---
title: Uso dei moduli sperimentali di Azure PowerShell
description: Informazioni sulla filosofia e sull'utilizzo dei moduli sperimentali di Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/11/2018
ms.openlocfilehash: 11847ca2fe09ebeb48f962eab6dac2be06bd8805
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/05/2020
ms.locfileid: "65534358"
---
# <a name="use-experimental-azure-powershell-modules"></a><span data-ttu-id="40b5a-103">Usare i moduli sperimentali di Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="40b5a-103">Use experimental Azure PowerShell modules</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="40b5a-104">In considerazione della particolare importanza attribuita agli strumenti di sviluppo e soprattutto alle interfacce della riga di comando in Azure, il team di Azure PowerShell sta sperimentando molti miglioramenti nell'esperienza di Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="40b5a-104">With the emphasis on developer tools (especially CLIs) in Azure, the Azure PowerShell team is experimenting with many improvements to the Azure PowerShell experience.</span></span>

## <a name="experimentation-methodology"></a><span data-ttu-id="40b5a-105">Metodologia di sperimentazione</span><span class="sxs-lookup"><span data-stu-id="40b5a-105">Experimentation methodology</span></span>

<span data-ttu-id="40b5a-106">Per agevolare la sperimentazione, vengono creati nuovi moduli di Azure PowerShell che implementano funzionalità esistenti di Azure SDK in nuovi modi più facili da usare.</span><span class="sxs-lookup"><span data-stu-id="40b5a-106">To facilitate experimentation, we're creating new Azure PowerShell modules that implement existing Azure SDK functionality in new, easier to use ways.</span></span> <span data-ttu-id="40b5a-107">Nella maggior parte dei casi, i cmdlet rispecchiano esattamente cmdlet esistenti.</span><span class="sxs-lookup"><span data-stu-id="40b5a-107">In most cases, the cmdlets exactly mirror existing cmdlets.</span></span> <span data-ttu-id="40b5a-108">I cmdlet sperimentali, tuttavia, offrono una notazione a sintassi abbreviata e valori predefiniti più intelligenti che semplificano la creazione e la gestione delle risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="40b5a-108">However, the experimental cmdlets provide a shorthand notation and smarter default values that make it easier to create and manage Azure resources.</span></span>

<span data-ttu-id="40b5a-109">Questi moduli possono essere installati side-by-side con i moduli di Azure PowerShell esistenti.</span><span class="sxs-lookup"><span data-stu-id="40b5a-109">These modules can be installed side by side with existing Azure PowerShell modules.</span></span> <span data-ttu-id="40b5a-110">I nomi dei cmdlet sono stati abbreviati per offrire nomi più corti ed evitare conflitti di nome con i cmdlet non sperimentali esistenti.</span><span class="sxs-lookup"><span data-stu-id="40b5a-110">The cmdlet names have been shortened to provide shorter names and avoid name conflicts with existing, non-experimental cmdlets.</span></span>

<span data-ttu-id="40b5a-111">I moduli sperimentali adottano la convenzione di denominazione seguente: `AzureRM.*.Experiments`.</span><span class="sxs-lookup"><span data-stu-id="40b5a-111">The experimental modules use the following naming convention: `AzureRM.*.Experiments`.</span></span> <span data-ttu-id="40b5a-112">Questa convenzione di denominazione è simile alla denominazione dei moduli in anteprima: `AzureRM.*.Preview`.</span><span class="sxs-lookup"><span data-stu-id="40b5a-112">This naming convention is similar to the naming of Preview modules: `AzureRM.*.Preview`.</span></span> <span data-ttu-id="40b5a-113">I moduli in anteprima differiscono da quelli sperimentali</span><span class="sxs-lookup"><span data-stu-id="40b5a-113">Preview modules differ from experimental modules.</span></span> <span data-ttu-id="40b5a-114">perché implementano nuove funzionalità dei servizi di Azure che sono disponibili solo come anteprima.</span><span class="sxs-lookup"><span data-stu-id="40b5a-114">Preview modules implement new functionality of Azure services that is only available as a Preview offering.</span></span> <span data-ttu-id="40b5a-115">I moduli in anteprima sostituiscono moduli di Azure PowerShell esistenti e usano gli stessi nomi per cmdlet e parametri.</span><span class="sxs-lookup"><span data-stu-id="40b5a-115">Preview modules replace existing Azure PowerShell modules and use the same cmdlet and parameter names.</span></span>

## <a name="how-to-install-an-experimental-module"></a><span data-ttu-id="40b5a-116">Come installare un modulo sperimentale</span><span class="sxs-lookup"><span data-stu-id="40b5a-116">How to install an experimental module</span></span>

<span data-ttu-id="40b5a-117">I moduli sperimentali vengono pubblicati in PowerShell Gallery così come i moduli di Azure PowerShell esistenti.</span><span class="sxs-lookup"><span data-stu-id="40b5a-117">Experimental modules are published to the PowerShell Gallery just like the existing Azure PowerShell modules.</span></span> <span data-ttu-id="40b5a-118">Per visualizzare un elenco di moduli sperimentali, eseguire questo comando:</span><span class="sxs-lookup"><span data-stu-id="40b5a-118">To see a list of experimental modules, run the following command:</span></span>

```azurepowershell-interactive
Find-Module AzureRM.*.Experiments
```

```output
Version Name                         Repository Description
------- ----                         ---------- -----------
1.0.25  AzureRM.Compute.Experiments  PSGallery  Azure Compute experiments for VM creation
1.0.0   AzureRM.Websites.Experiments PSGallery  Create and deploy web applications using Azure App Services.
```

<span data-ttu-id="40b5a-119">Per installare il modulo sperimentale, usare i comandi seguenti in una sessione di PowerShell con privilegi elevati:</span><span class="sxs-lookup"><span data-stu-id="40b5a-119">To install the experimental module, use the following commands from an elevated PowerShell session:</span></span>

```azurepowershell-interactive
Install-Module AzureRM.Compute.Experiments
Install-Module AzureRM.Websites.Experiments
```

### <a name="documentation-and-support"></a><span data-ttu-id="40b5a-120">Documentazione e supporto</span><span class="sxs-lookup"><span data-stu-id="40b5a-120">Documentation and support</span></span>

<span data-ttu-id="40b5a-121">La documentazione è inclusa nel pacchetto di installazione ed è accessibile con il cmdlet `Get-Help`.</span><span class="sxs-lookup"><span data-stu-id="40b5a-121">Documentation is included in the install package and is accessed using the `Get-Help` cmdlet.</span></span> <span data-ttu-id="40b5a-122">Per i moduli sperimentali non viene pubblicata documentazione ufficiale.</span><span class="sxs-lookup"><span data-stu-id="40b5a-122">No official documentation is published for experimental modules.</span></span>

<span data-ttu-id="40b5a-123">Gli utenti sono invitati a testare questi moduli</span><span class="sxs-lookup"><span data-stu-id="40b5a-123">We encourage you to test these modules.</span></span> <span data-ttu-id="40b5a-124">e inviare commenti e suggerimenti, che consentiranno di migliorare l'usabilità e soddisfare le esigenze.</span><span class="sxs-lookup"><span data-stu-id="40b5a-124">Your feedback allows us to improve usability and respond to your needs.</span></span> <span data-ttu-id="40b5a-125">Dato che sono sperimentali, tuttavia, il supporto per questi moduli è limitato.</span><span class="sxs-lookup"><span data-stu-id="40b5a-125">However, being experimental, support for these modules is limited.</span></span> <span data-ttu-id="40b5a-126">È possibile inviare domande o segnalare problemi creando un [problema](https://github.com/Azure/azure-powershell/issues) nel repository GitHub.</span><span class="sxs-lookup"><span data-stu-id="40b5a-126">Questions or problem reports can be submitted by creating an [issue](https://github.com/Azure/azure-powershell/issues) in the GitHub repository.</span></span>

## <a name="experiments-and-areas-of-improvement"></a><span data-ttu-id="40b5a-127">Esperimenti e aree di miglioramento</span><span class="sxs-lookup"><span data-stu-id="40b5a-127">Experiments and areas of improvement</span></span>

<span data-ttu-id="40b5a-128">Questi miglioramenti sono stati selezionati in base agli elementi di differenziazione chiave nei prodotti concorrenti.</span><span class="sxs-lookup"><span data-stu-id="40b5a-128">These improvements were selected based on key differentiators in competing products.</span></span> <span data-ttu-id="40b5a-129">Uno degli obiettivi dell'interfaccia della riga di comando di Azure 2.0, ad esempio, è stato basare i comandi su _scenari_ anziché sulla _superficie di attacco dell'API_.</span><span class="sxs-lookup"><span data-stu-id="40b5a-129">For example, Azure CLI 2.0 has made a point of basing commands on _scenarios_ rather than _API surface area_.</span></span>
<span data-ttu-id="40b5a-130">L'interfaccia della riga di comando di Azure 2.0 usa diverse impostazioni predefinite intelligenti che semplificano gli scenari "introduttivi" per gli utenti finali.</span><span class="sxs-lookup"><span data-stu-id="40b5a-130">Azure CLI 2.0 use a number of smart defaults that make "getting started" scenarios easier for end users.</span></span>

### <a name="core-improvements"></a><span data-ttu-id="40b5a-131">Miglioramenti di base</span><span class="sxs-lookup"><span data-stu-id="40b5a-131">Core improvements</span></span>

<span data-ttu-id="40b5a-132">I miglioramenti di base sono considerati "buon senso" e non è necessaria molta sperimentazione per procedere all'implementazione di questi aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="40b5a-132">The core improvements are regarded as "common sense", and little experimentation is needed to move forward in implementing these updates.</span></span>

- <span data-ttu-id="40b5a-133">Cmdlet basati su scenari: i cmdlet <em>\*All</em>- dovranno essere progettati sulla base di scenari, non del servizio REST di Azure.</span><span class="sxs-lookup"><span data-stu-id="40b5a-133">Scenario-based Cmdlets - <em>\*All</em>- cmdlets should be designed around scenarios, not the Azure REST service.</span></span>

- <span data-ttu-id="40b5a-134">Nomi più brevi: include i nomi dei cmdlet (ad esempio, `New-AzureRmVM` => `New-AzVm`) e dei parametri (ad esempio, `-ResourceGroupName` => `-Rg`).</span><span class="sxs-lookup"><span data-stu-id="40b5a-134">Shorter Names - Includes the names of cmdlets (for example, `New-AzureRmVM` => `New-AzVm`) and the names of parameters (for example, `-ResourceGroupName` => `-Rg`).</span></span> <span data-ttu-id="40b5a-135">Usare alias per la compatibilità con i cmdlet "meno recenti"</span><span class="sxs-lookup"><span data-stu-id="40b5a-135">Use aliases for compatibility with "old" cmdlets.</span></span> <span data-ttu-id="40b5a-136">e specificare set di parametri _compatibili con le versioni precedenti_.</span><span class="sxs-lookup"><span data-stu-id="40b5a-136">Provide _backwards compatible_ parameter sets.</span></span>

- <span data-ttu-id="40b5a-137">Impostazioni predefinite intelligenti: creare impostazioni predefinite intelligenti per immettere le informazioni "necessarie",</span><span class="sxs-lookup"><span data-stu-id="40b5a-137">Smart Defaults - Create smart defaults to fill in "required" information.</span></span> <span data-ttu-id="40b5a-138">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="40b5a-138">For example:</span></span>
  - <span data-ttu-id="40b5a-139">Gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="40b5a-139">Resource Group</span></span>
  - <span data-ttu-id="40b5a-140">Location</span><span class="sxs-lookup"><span data-stu-id="40b5a-140">Location</span></span>
  - <span data-ttu-id="40b5a-141">Risorse dipendenti</span><span class="sxs-lookup"><span data-stu-id="40b5a-141">Dependent resources</span></span>

### <a name="experimental-improvements"></a><span data-ttu-id="40b5a-142">Miglioramenti sperimentali</span><span class="sxs-lookup"><span data-stu-id="40b5a-142">Experimental improvements</span></span>

<span data-ttu-id="40b5a-143">I miglioramenti sperimentali presentano un cambiamento significativo che il team vuole convalidare tramite la sperimentazione.</span><span class="sxs-lookup"><span data-stu-id="40b5a-143">The experimental improvements present a significant change that the team wants to validate via experimentation.</span></span>

- <span data-ttu-id="40b5a-144">Tipi semplici: per gli scenari di creazione non dovranno più essere usati tipi complessi e oggetti di configurazione.</span><span class="sxs-lookup"><span data-stu-id="40b5a-144">Simple types - Create scenarios should move away from complex types and config objects.</span></span> <span data-ttu-id="40b5a-145">Semplificare la configurazione riducendola a uno o due parametri.</span><span class="sxs-lookup"><span data-stu-id="40b5a-145">Simplify the configuration down to one or two parameters.</span></span>

- <span data-ttu-id="40b5a-146">"Creazione intelligente": tutti gli scenari di creazione che implementano la "creazione intelligente" _non_ avranno parametro obbligatori. Tutte le informazioni necessarie verranno scelte autonomamente da Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="40b5a-146">"Smart Create" - All create scenarios implementing "Smart Create" would have _no_ required parameters: all necessary information would be chosen by Azure PowerShell in an opinionated fashion.</span></span>

- <span data-ttu-id="40b5a-147">Parametri "grigi": in molti casi, alcuni parametri potrebbero essere "grigi" o semifacoltativi.</span><span class="sxs-lookup"><span data-stu-id="40b5a-147">Gray Parameters - In many cases, some parameters could be "gray" or semi-optional.</span></span> <span data-ttu-id="40b5a-148">Se il parametro non viene specificato, all'utente viene chiesto se vuole che venga generato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="40b5a-148">If the parameter isn't specified, the user is asked if they want the parameter generated for them.</span></span> <span data-ttu-id="40b5a-149">È anche opportuno che il valore per i parametri "grigi" venga dedotto in base al contesto con il consenso dell'utente,</span><span class="sxs-lookup"><span data-stu-id="40b5a-149">It also makes sense for gray parameters to infer a value based on context with the user's consent.</span></span>
  <span data-ttu-id="40b5a-150">ad esempio suggerendo il valore usato di recente.</span><span class="sxs-lookup"><span data-stu-id="40b5a-150">For example, it may make sense to have the gray parameter suggest the most recently used value.</span></span>

- <span data-ttu-id="40b5a-151">Opzione `-Auto`: l'opzione `-Auto` offrirà agli utenti la possibilità di "acconsentire esplicitamente" all'_impostazione predefinita di tutti i valori_ mantenendo al tempo stesso l'integrità dei parametri obbligatori nel percorso principale.</span><span class="sxs-lookup"><span data-stu-id="40b5a-151">`-Auto` Switch - The `-Auto` switch would provide an "opt-in" way for users to _default all the things_ while maintaining the integrity of required parameters in the mainline path.</span></span>

### <a name="feature-specific-switches"></a><span data-ttu-id="40b5a-152">Opzioni specifiche delle funzionalità</span><span class="sxs-lookup"><span data-stu-id="40b5a-152">Feature-specific switches</span></span>

<span data-ttu-id="40b5a-153">Lo scenario di creazione di app Web, ad esempio, potrebbe avere un'opzione `-Git` o `-AddRemote` che aggiungerà automaticamente un'istanza remota di Azure a un repository Git esistente.</span><span class="sxs-lookup"><span data-stu-id="40b5a-153">For example, the "Create web app" scenario might have a `-Git` or `-AddRemote` switch that would automatically add an "azure" remote to an existing git repository.</span></span>

- <span data-ttu-id="40b5a-154">Valori predefiniti impostabili: gli utenti dovranno avere la possibilità di impostare valori predefiniti per parametri comuni come `-ResourceGroupName` e `-Location`.</span><span class="sxs-lookup"><span data-stu-id="40b5a-154">Settable Defaults - Users should be able to set defaults for common parameters like `-ResourceGroupName` and `-Location`.</span></span>

- <span data-ttu-id="40b5a-155">Impostazioni predefinite per le dimensioni: le "dimensioni" delle risorse possono confondere gli utenti perché molti provider di risorse usano nomi diversi, ad esempio "Standard\_DS1\_v2" o "S1".</span><span class="sxs-lookup"><span data-stu-id="40b5a-155">Size Defaults - Resource "sizes" can be confusing to users since many Resource Providers use different names (for example, "Standard\_DS1\_v2" or "S1").</span></span> <span data-ttu-id="40b5a-156">La maggior parte degli utenti, tuttavia presta molta attenzione al costo.</span><span class="sxs-lookup"><span data-stu-id="40b5a-156">However, most users care more about cost.</span></span> <span data-ttu-id="40b5a-157">È quindi opportuno definire dimensioni "universali" in base a una pianificazione prezzi.</span><span class="sxs-lookup"><span data-stu-id="40b5a-157">So it makes sense to define "universal" sizes based on a pricing schedule.</span></span> <span data-ttu-id="40b5a-158">Gli utenti possono scegliere dimensioni specifiche o lasciare che Azure PowerShell scelga l'_opzione migliore_ in base alla risorsa e al budget.</span><span class="sxs-lookup"><span data-stu-id="40b5a-158">Users can choose a specific size or let Azure PowerShell choose the _best option_ based on the resource the budget.</span></span>

- <span data-ttu-id="40b5a-159">Formato di output: Azure PowerShell attualmente restituisce oggetti `PSObject` e l'output della console è ridotto.</span><span class="sxs-lookup"><span data-stu-id="40b5a-159">Output Format - Azure PowerShell currently returns `PSObject`s and there's little console output.</span></span> <span data-ttu-id="40b5a-160">Potrebbe essere necessario visualizzare all'utente in Azure PowerShell alcune informazioni sulle impostazioni predefinite intelligenti usate.</span><span class="sxs-lookup"><span data-stu-id="40b5a-160">Azure PowerShell may need to display some information to the user about the "smart defaults" used.</span></span>
