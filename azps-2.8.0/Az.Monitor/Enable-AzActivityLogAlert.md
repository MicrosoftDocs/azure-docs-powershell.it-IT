---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: fb3407046970a3341b7eb5d6f28ed2f2d682126f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673827"
---
# <span data-ttu-id="2c571-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2c571-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="2c571-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c571-102">SYNOPSIS</span></span>
<span data-ttu-id="2c571-103">Abilita un avviso del log attività e ne imposta i contrassegni.</span><span class="sxs-lookup"><span data-stu-id="2c571-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="2c571-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c571-104">SYNTAX</span></span>

### <span data-ttu-id="2c571-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2c571-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c571-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="2c571-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c571-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="2c571-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c571-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c571-108">DESCRIPTION</span></span>
<span data-ttu-id="2c571-109">Il cmdlet **Enable-AzActivityLogAlert** consente di abilitare un avviso del log attività e di impostarne i contrassegni.</span><span class="sxs-lookup"><span data-stu-id="2c571-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="2c571-110">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere la conferma da parte dell'utente prima di applicare la patch alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="2c571-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="2c571-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c571-111">EXAMPLES</span></span>

### <span data-ttu-id="2c571-112">Esempio 1: abilitare un avviso del log attività</span><span class="sxs-lookup"><span data-stu-id="2c571-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="2c571-113">Questo comando Abilita l'avviso del log attività denominato Alert1 nel gruppo di risorse predefinito-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="2c571-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="2c571-114">Esempio 2: abilitare un avviso del log attività usando un oggetto PSActivityLogAlertResource come input</span><span class="sxs-lookup"><span data-stu-id="2c571-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="2c571-115">Questo comando Abilita l'avviso di un log attività denominato Alert1.</span><span class="sxs-lookup"><span data-stu-id="2c571-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="2c571-116">Per questo usa un oggetto PSActivityLogAlertResource come argomento di input.</span><span class="sxs-lookup"><span data-stu-id="2c571-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="2c571-117">Esempio 3: abilitare il ActivityLogAlert usando il parametro ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c571-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="2c571-118">Questo comando consente a ActivityLogAlert di usare il parametro ResourceId dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="2c571-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="2c571-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c571-119">PARAMETERS</span></span>

### <span data-ttu-id="2c571-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c571-120">-DefaultProfile</span></span>
<span data-ttu-id="2c571-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="2c571-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c571-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c571-122">-InputObject</span></span>
<span data-ttu-id="2c571-123">Imposta la proprietà Tag InputObject della chiamata per estrarre il nome necessario, il nome del gruppo di risorse e le proprietà facoltative dei tag.</span><span class="sxs-lookup"><span data-stu-id="2c571-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: EnableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c571-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="2c571-124">-Name</span></span>
<span data-ttu-id="2c571-125">Nome dell'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="2c571-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c571-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c571-126">-ResourceGroupName</span></span>
<span data-ttu-id="2c571-127">Nome del gruppo di risorse in cui sta per esistere la risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="2c571-127">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c571-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c571-128">-ResourceId</span></span>
<span data-ttu-id="2c571-129">Imposta la proprietà ResourceId tag della chiamata per estrarre le proprietà nome obbligatorio, nome gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="2c571-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c571-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2c571-130">-Confirm</span></span>
<span data-ttu-id="2c571-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c571-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c571-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c571-132">-WhatIf</span></span>
<span data-ttu-id="2c571-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2c571-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c571-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2c571-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c571-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c571-135">CommonParameters</span></span>
<span data-ttu-id="2c571-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c571-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c571-137">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c571-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c571-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c571-138">INPUTS</span></span>

### <span data-ttu-id="2c571-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2c571-139">System.String</span></span>

### <span data-ttu-id="2c571-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="2c571-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="2c571-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c571-141">OUTPUTS</span></span>

### <span data-ttu-id="2c571-142">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="2c571-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="2c571-143">Note</span><span class="sxs-lookup"><span data-stu-id="2c571-143">NOTES</span></span>

## <span data-ttu-id="2c571-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c571-144">RELATED LINKS</span></span>

[<span data-ttu-id="2c571-145">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2c571-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="2c571-146">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2c571-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="2c571-147">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2c571-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="2c571-148">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="2c571-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="2c571-149">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="2c571-149">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

[<span data-ttu-id="2c571-150">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2c571-150">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)