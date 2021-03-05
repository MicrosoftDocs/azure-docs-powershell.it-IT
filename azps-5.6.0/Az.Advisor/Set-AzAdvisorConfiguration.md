---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Advisor.dll-Help.xml
Module Name: Az.Advisor
online version: https://docs.microsoft.com/powershell/module/az.advisor/set-azadvisorConfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Advisor/Advisor/help/Set-AzAdvisorConfiguration.md
ms.openlocfilehash: 550b9d11cd2f5b0cadb13d76809faa2ac34dc426
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966990"
---
# <span data-ttu-id="a8a34-101">Set-AzAdvisorConfiguration</span><span class="sxs-lookup"><span data-stu-id="a8a34-101">Set-AzAdvisorConfiguration</span></span>

## <span data-ttu-id="a8a34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8a34-102">SYNOPSIS</span></span>
<span data-ttu-id="a8a34-103">Aggiorna o crea la configurazione di Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="a8a34-103">Updates or creates the Azure Advisor Configuration.</span></span>

## <span data-ttu-id="a8a34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8a34-104">SYNTAX</span></span>

### <span data-ttu-id="a8a34-105">InputObjectRgExcludeParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a8a34-105">InputObjectRgExcludeParameterSet (Default)</span></span>
```
Set-AzAdvisorConfiguration [-Exclude] [[-ResourceGroupName] <String>]
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8a34-106">InputObjectLowCpuExcludeParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8a34-106">InputObjectLowCpuExcludeParameterSet</span></span> 
```
Set-AzAdvisorConfiguration [-Exclude] [-LowCpuThreshold] <Int32>
 [[-InputObject] <PsAzureAdvisorConfigurationData>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8a34-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a8a34-107">DESCRIPTION</span></span>
<span data-ttu-id="a8a34-108">Usato per aggiornare la configurazione di Azure Advisor.</span><span class="sxs-lookup"><span data-stu-id="a8a34-108">Used to update the configuration of the Azure Advisor.</span></span> <span data-ttu-id="a8a34-109">Sono presenti due tipi di configurazione: configurazione a livello di abbonamento e configurazione a livello di Gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a8a34-109">Two types of Configuration are present: Subscription level configuration and ResourceGroup level configuration.</span></span> 

<span data-ttu-id="a8a34-110">Configurazione a livello di abbonamento: per una sottoscrizione può essere presente una sola configurazione per questo tipo.</span><span class="sxs-lookup"><span data-stu-id="a8a34-110">Subscription level configuration: There can be only one Configuration for this type for a subscription.</span></span> <span data-ttu-id="a8a34-111">Le proprietà LowCpuThreshold ed Exclude possono essere aggiornate con questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8a34-111">LowCpuThreshold and Exclude properties can be updated using this cmdlet.</span></span>
<span data-ttu-id="a8a34-112">Configurazione a livello di Gruppo Risorse: può essere presente una sola configurazione per ogni ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="a8a34-112">ResourceGroup level configuration: There can be only one configuration for each ResourceGroup.</span></span> <span data-ttu-id="a8a34-113">Solo la proprietà Exclude può essere aggiornata con questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8a34-113">Only Exclude property can be updated using this cmdlet.</span></span>

## <span data-ttu-id="a8a34-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8a34-114">EXAMPLES</span></span>

###  <span data-ttu-id="a8a34-115">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a8a34-115">Example 1</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 10
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 10

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="a8a34-116">Aggiorna la configurazione(lowCpuThreshold) per la configurazione a livello di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a8a34-116">Updates the configuration(lowCpuThreshold) for subscription level Configuration.</span></span>

### <span data-ttu-id="a8a34-117">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a8a34-117">Example 2</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -LowCpuThreshold 15 -Exclude 
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : 15

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="a8a34-118">Aggiorna la configurazione(lowCpuThreshold, exclude) per la configurazione a livello di sottoscrizione e le esclusive dalla generazione di consigli.</span><span class="sxs-lookup"><span data-stu-id="a8a34-118">Updates the configuration(lowCpuThreshold, exclude) for subscription level Configuration and excludes from the recommendation generation.</span></span>

### <span data-ttu-id="a8a34-119">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a8a34-119">Example 3</span></span>
```powershell
PS C:\> Set-AzAdvisorConfiguration -ResourceGroupName resourceGroupName1 -Exclude

Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}-resourceGroupName1
Name       : {user_subscription}-resourceGroupName1
Properties : additionalProperties : null
             exclude :  True
             lowCpuThreshold : null

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="a8a34-120">Aggiorna la configurazione(exclude) per resourceGroupName1 da escludere nella generazione di consigli.</span><span class="sxs-lookup"><span data-stu-id="a8a34-120">Updates the configuration(exclude) for resourceGroupName1 to be excluded in the recommendation generation.</span></span>

### <span data-ttu-id="a8a34-121">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="a8a34-121">Example 4</span></span>
```powershell
PS C:\> Get-AzAdvisorConfiguration | Set-AzAdvisorConfiguration -LowCpuThreshold 20
Id         : /subscriptions/{user_subscription}/resourceGroups/resourceGroupName1/providers/Microsoft.Advisor/configurations/{user_subscription}
Name       : {user_subscription}
Properties : additionalProperties : null
             exclude :  False
             lowCpuThreshold : 20

Type       : Microsoft.Advisor/Configurations
```

<span data-ttu-id="a8a34-122">Aggiorna la configurazione per il suggerimento specificato passato dalla pipeline.</span><span class="sxs-lookup"><span data-stu-id="a8a34-122">Updates the configuration for the given recommendation passed on from the pipeline.</span></span>

## <span data-ttu-id="a8a34-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8a34-123">PARAMETERS</span></span>

### <span data-ttu-id="a8a34-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8a34-124">-Confirm</span></span>
<span data-ttu-id="a8a34-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8a34-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8a34-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8a34-126">-DefaultProfile</span></span>
<span data-ttu-id="a8a34-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8a34-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8a34-128">-Exclude</span><span class="sxs-lookup"><span data-stu-id="a8a34-128">-Exclude</span></span>
<span data-ttu-id="a8a34-129">Escludere dalla generazione di suggerimenti.</span><span class="sxs-lookup"><span data-stu-id="a8a34-129">Exclude from the recommendation generation.</span></span> <span data-ttu-id="a8a34-130">Se la proprietà di esclusione non specificata viene impostata su false.</span><span class="sxs-lookup"><span data-stu-id="a8a34-130">If not specified exclude property will be set to false.</span></span>

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

### <span data-ttu-id="a8a34-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8a34-131">-InputObject</span></span>
<span data-ttu-id="a8a34-132">Il tipo di oggetto di PowerShell PsAzureAdvisorConfigurationData restituito dalla Get-AzAdvisorConfiguration chiamata.</span><span class="sxs-lookup"><span data-stu-id="a8a34-132">The powershell object type PsAzureAdvisorConfigurationData returned by Get-AzAdvisorConfiguration call.</span></span>

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

### <span data-ttu-id="a8a34-133">-LowCpuThreshold</span><span class="sxs-lookup"><span data-stu-id="a8a34-133">-LowCpuThreshold</span></span>
<span data-ttu-id="a8a34-134">Valore per la soglia della CPU bassa.</span><span class="sxs-lookup"><span data-stu-id="a8a34-134">Value for Low Cpu threshold.</span></span>

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

### <span data-ttu-id="a8a34-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8a34-135">-ResourceGroupName</span></span>
<span data-ttu-id="a8a34-136">Nome del gruppo di risorse per la configurazione.</span><span class="sxs-lookup"><span data-stu-id="a8a34-136">Resource Group name for the configuration.</span></span>

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

### <span data-ttu-id="a8a34-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8a34-137">-WhatIf</span></span>
<span data-ttu-id="a8a34-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8a34-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8a34-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8a34-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8a34-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8a34-140">CommonParameters</span></span>
<span data-ttu-id="a8a34-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8a34-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a8a34-142">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8a34-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8a34-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="a8a34-143">INPUTS</span></span>

### <span data-ttu-id="a8a34-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="a8a34-144">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="a8a34-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8a34-145">OUTPUTS</span></span>

### <span data-ttu-id="a8a34-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span><span class="sxs-lookup"><span data-stu-id="a8a34-146">Microsoft.Azure.Commands.Advisor.Cmdlets.Models.PsAzureAdvisorConfigurationData</span></span>

## <span data-ttu-id="a8a34-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="a8a34-147">NOTES</span></span>

## <span data-ttu-id="a8a34-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8a34-148">RELATED LINKS</span></span>
