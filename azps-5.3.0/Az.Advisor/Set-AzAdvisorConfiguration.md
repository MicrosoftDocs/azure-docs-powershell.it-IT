---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/en-us/powershell/module/az.advisor/set-azadvisorConfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
ms.openlocfilehash: bfd1677fa46a749b73206b02bb6585c4a529637f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98479139"
---
# <span data-ttu-id="14d4d-101">Set-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="14d4d-101">Set-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="14d4d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="14d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="14d4d-103">Aggiorna o crea la configurazione di Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="14d4d-103">Updates or creates the Azure Advisor Configuration.</span></span>

## <span data-ttu-id="14d4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14d4d-104">SYNTAX</span></span>

### <span data-ttu-id="14d4d-105">InputObjectRgExcludeParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="14d4d-105">InputObjectRgExcludeParameterSet (Default)</span></span>
```
Set-AzAdvisorConfiguration [-Exclude] [[-ResourceGroupName] <String>]
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14d4d-106">InputObjectLowCpuExcludeParameterSet</span><span class="sxs-lookup"><span data-stu-id="14d4d-106">InputObjectLowCpuExcludeParameterSet</span></span> 
```
Set-AzAdvisorConfiguration [-Exclude] [-LowCpuThreshold] <Int32>
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14d4d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14d4d-107">DESCRIPTION</span></span>
<span data-ttu-id="14d4d-108">Usato per aggiornare la configurazione di Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="14d4d-108">Used to update the configuration of the Azure Advisor.</span></span> <span data-ttu-id="14d4d-109">Sono presenti due tipi di configurazione: configurazione a livello di abbonamento e configurazione a livello di ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="14d4d-109">Two types of Configuration are present: Subscription level configuration and ResourceGroup level configuration.</span></span> 

<span data-ttu-id="14d4d-110">Configurazione a livello di abbonamento: può essere disponibile una sola configurazione per questo tipo per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="14d4d-110">Subscription level configuration: There can be only one Configuration for this type for a subscription.</span></span> <span data-ttu-id="14d4d-111">Le proprietà LowCpuThreshold ed exclude possono essere aggiornate con questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14d4d-111">LowCpuThreshold and Exclude properties can be updated using this cmdlet.</span></span>
<span data-ttu-id="14d4d-112">Configurazione a livello di ResourceGroup: può essere disponibile una sola configurazione per ogni ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="14d4d-112">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup.</span></span> <span data-ttu-id="14d4d-113">Solo la proprietà Exclude può essere aggiornata usando questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14d4d-113">Only Exclude property can be updated using this cmdlet.</span></span>

## <span data-ttu-id="14d4d-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14d4d-114">EXAMPLES</span></span>

###  <span data-ttu-id="14d4d-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="14d4d-115">Example 1</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 10
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 10

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="14d4d-116">Aggiorna la configurazione (lowCpuThreshold) per la configurazione a livello di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="14d4d-116">Updates the configuration(lowCpuThreshold) for subscription level Configuration.</span></span>

### <span data-ttu-id="14d4d-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="14d4d-117">Example 2</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 15 -Exclude 
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : 15

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="14d4d-118">Aggiorna la configurazione (lowCpuThreshold, Exclude) per la configurazione del livello di sottoscrizione ed esclude dalla generazione di raccomandazioni.</span><span class="sxs-lookup"><span data-stu-id="14d4d-118">Updates the configuration(lowCpuThreshold, exclude) for subscription level Configuration and excludes from the recommendation generation.</span></span>

### <span data-ttu-id="14d4d-119">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="14d4d-119">Example 3</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -ResourceGroupName resourceGroupName1 -Exclude

Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}-resourceGroupName1
Name       : {user_subscription}-resourceGroupName1
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : null

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="14d4d-120">Aggiorna la configurazione (Escludi) per resourceGroupName1 da escludere nella generazione di raccomandazioni.</span><span class="sxs-lookup"><span data-stu-id="14d4d-120">Updates the configuration(exclude) for resourceGroupName1 to be excluded in the recommendation generation.</span></span>

### <span data-ttu-id="14d4d-121">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="14d4d-121">Example 4</span></span>
```powershell
PS C:\> Get-AzAdvisorConfiguration | Set-AzAdvisorConfiguration -LowCpuThreshold 20
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 20

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="14d4d-122">Aggiorna la configurazione per la raccomandazione specificata passata dalla pipeline.</span><span class="sxs-lookup"><span data-stu-id="14d4d-122">Updates the configuration for the given recommendation passed on from the pipeline.</span></span>

## <span data-ttu-id="14d4d-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="14d4d-123">PARAMETERS</span></span>

### <span data-ttu-id="14d4d-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="14d4d-124">-Confirm</span></span>
<span data-ttu-id="14d4d-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14d4d-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14d4d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14d4d-126">-DefaultProfile</span></span>
<span data-ttu-id="14d4d-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14d4d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14d4d-128">-Escludi</span><span class="sxs-lookup"><span data-stu-id="14d4d-128">-Exclude</span></span>
<span data-ttu-id="14d4d-129">Escludere dalla generazione di raccomandazioni.</span><span class="sxs-lookup"><span data-stu-id="14d4d-129">Exclude from the recommendation generation.</span></span> <span data-ttu-id="14d4d-130">Se la proprietà Exclude non specificata verrà impostata su false.</span><span class="sxs-lookup"><span data-stu-id="14d4d-130">If not specified exclude property will be set to false.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14d4d-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14d4d-131">-InputObject</span></span>
<span data-ttu-id="14d4d-132">Il tipo di oggetto PowerShell PsAzureAdvisorConfigurationData restituito da Get-AzAdvisorConfiguration chiamata.</span><span class="sxs-lookup"><span data-stu-id="14d4d-132">The powershell object type PsAzureAdvisorConfigurationData returned by Get-AzAdvisorConfiguration call.</span></span>

```yaml
Type: PsAzureAdvisorConfigurationData
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14d4d-133">-LowCpuThreshold</span><span class="sxs-lookup"><span data-stu-id="14d4d-133">-LowCpuThreshold</span></span>
<span data-ttu-id="14d4d-134">Valore per la soglia minima della CPU.</span><span class="sxs-lookup"><span data-stu-id="14d4d-134">Value for Low Cpu threshold.</span></span>

```yaml
Type: Int32
Parameter Sets: InputObjectLowCpuExcludeParameterSet
Aliases:
Accepted values: 0, 5, 10, 15, 20

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14d4d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14d4d-135">-ResourceGroupName</span></span>
<span data-ttu-id="14d4d-136">Nome del gruppo di risorse per la configurazione.</span><span class="sxs-lookup"><span data-stu-id="14d4d-136">Resource Group name for the configuration.</span></span>

```yaml
Type: String
Parameter Sets: InputObjectRgExcludeParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14d4d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14d4d-137">-WhatIf</span></span>
<span data-ttu-id="14d4d-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14d4d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14d4d-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14d4d-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14d4d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14d4d-140">CommonParameters</span></span>
<span data-ttu-id="14d4d-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14d4d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="14d4d-142">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14d4d-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14d4d-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="14d4d-143">INPUTS</span></span>

### <span data-ttu-id="14d4d-144">Microsoft. Azure. Commands. Advisor. Cmdlets. Models. PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="14d4d-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="14d4d-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14d4d-145">OUTPUTS</span></span>

### <span data-ttu-id="14d4d-146">Microsoft. Azure. Commands. Advisor. Cmdlets. Models. PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="14d4d-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="14d4d-147">Note</span><span class="sxs-lookup"><span data-stu-id="14d4d-147">NOTES</span></span>

## <span data-ttu-id="14d4d-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14d4d-148">RELATED LINKS</span></span>
