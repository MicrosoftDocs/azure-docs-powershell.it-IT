---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Disable-AzIotSecurityAnalyticsAggregatedAlert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Disable-AzIotSecurityAnalyticsAggregatedAlert.md
ms.openlocfilehash: 3747109d13fd4224b0f86bc5ecf2992ed4229487
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191958"
---
# <span data-ttu-id="ae759-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="ae759-101">Disable-AzIotSecurityAnalyticsAggregatedAlert</span></span>

## <span data-ttu-id="ae759-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae759-102">SYNOPSIS</span></span>
<span data-ttu-id="ae759-103">Respingere l'avviso aggregato di un sacco</span><span class="sxs-lookup"><span data-stu-id="ae759-103">Dismiss Iot aggregated alert</span></span>

## <span data-ttu-id="ae759-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae759-104">SYNTAX</span></span>

### <span data-ttu-id="ae759-105">SolutionLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ae759-105">SolutionLevelResource (Default)</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName <String> -SolutionName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae759-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ae759-106">InputObject</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -InputObject <PSIoTSecurityAggregatedAlert> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae759-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae759-107">ResourceId</span></span>
```
Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae759-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae759-108">DESCRIPTION</span></span>
<span data-ttu-id="ae759-109">Il cmdlet Disable-AzIotSecurityAnalyticsAggregatedAlert respinge un avviso di aggragated specifico nei dispositivi di hub degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="ae759-109">The Disable-AzIotSecurityAnalyticsAggregatedAlert cmdlet dismisses a specific aggragated alert on devices of iot hub.</span></span> <span data-ttu-id="ae759-110">Il nome degli avvisi aggregati è una combinazione del tipo di avviso e della data di aggragted di avviso, separati da "/".</span><span class="sxs-lookup"><span data-stu-id="ae759-110">The name of the aggregated alerts is a combination of the alert type and the alert aggragted date, separated by '/'.</span></span>

## <span data-ttu-id="ae759-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae759-111">EXAMPLES</span></span>

### <span data-ttu-id="ae759-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ae759-112">Example 1</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceGroupName "MyResourceGroup" -SolutionName "MySolutionName" -Name "IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="ae759-113">Respingere l'avviso aggregato "IoT_SucessfulLocalLogin/2020-03-15" (nome combinato da tipo di avviso e data di aggregazione) dalla soluzione di sicurezza per gli altri dati "nome di soluzione" nel gruppo di risorse "MyResourceGroup"</span><span class="sxs-lookup"><span data-stu-id="ae759-113">Dismiss aggregated alert "IoT_SucessfulLocalLogin/2020-03-15" (name combined from alert type and its aggregated date) from the IoT security solution "MySolutionName" in resource group "MyResourceGroup"</span></span>

### <span data-ttu-id="ae759-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ae759-114">Example 2</span></span>
```powershell
PS C:\> Disable-AzIotSecurityAnalyticsAggregatedAlert -ResourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"
```

<span data-ttu-id="ae759-115">Ignorare l'avviso aggregato con l'ID risorsa "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span><span class="sxs-lookup"><span data-stu-id="ae759-115">Dismiss aggregated alert with resource Id "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Security/iotSecuritySolutions/MySolutionName/analyticsModels/default/aggregatedAlerts/IoT_SucessfulLocalLogin/2020-03-15"</span></span>

## <span data-ttu-id="ae759-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae759-116">PARAMETERS</span></span>

### <span data-ttu-id="ae759-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae759-117">-DefaultProfile</span></span>
<span data-ttu-id="ae759-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ae759-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae759-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae759-119">-InputObject</span></span>
<span data-ttu-id="ae759-120">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="ae759-120">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae759-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae759-121">-Name</span></span>
<span data-ttu-id="ae759-122">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="ae759-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae759-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae759-123">-PassThru</span></span>
<span data-ttu-id="ae759-124">Restituirà se l'operazione è stata eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="ae759-124">Return whether the operation was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae759-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae759-125">-ResourceGroupName</span></span>
<span data-ttu-id="ae759-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ae759-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae759-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae759-127">-ResourceId</span></span>
<span data-ttu-id="ae759-128">ID della risorsa di sicurezza a cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="ae759-128">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae759-129">-SolutionName</span><span class="sxs-lookup"><span data-stu-id="ae759-129">-SolutionName</span></span>
<span data-ttu-id="ae759-130">Nome soluzione</span><span class="sxs-lookup"><span data-stu-id="ae759-130">Solution name</span></span>

```yaml
Type: System.String
Parameter Sets: SolutionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae759-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ae759-131">-Confirm</span></span>
<span data-ttu-id="ae759-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae759-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae759-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae759-133">-WhatIf</span></span>
<span data-ttu-id="ae759-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae759-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae759-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae759-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae759-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae759-136">CommonParameters</span></span>
<span data-ttu-id="ae759-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae759-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae759-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ae759-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae759-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae759-139">INPUTS</span></span>

### <span data-ttu-id="ae759-140">Microsoft. Azure. Commands. Security. Models. IotSecuritySolutionAnalytics. PSIoTSecurityAggregatedAlert</span><span class="sxs-lookup"><span data-stu-id="ae759-140">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutionAnalytics.PSIoTSecurityAggregatedAlert</span></span>

### <span data-ttu-id="ae759-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ae759-141">System.String</span></span>

## <span data-ttu-id="ae759-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae759-142">OUTPUTS</span></span>

### <span data-ttu-id="ae759-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ae759-143">System.Boolean</span></span>

## <span data-ttu-id="ae759-144">Note</span><span class="sxs-lookup"><span data-stu-id="ae759-144">NOTES</span></span>

## <span data-ttu-id="ae759-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae759-145">RELATED LINKS</span></span>
