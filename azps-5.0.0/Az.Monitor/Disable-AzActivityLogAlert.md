---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/disable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
ms.openlocfilehash: bdd854d3f9cc17071e17fea232b1d872b0a5fe8a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203507"
---
# <span data-ttu-id="3e954-101">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3e954-101">Disable-AzActivityLogAlert</span></span>

## <span data-ttu-id="3e954-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3e954-102">SYNOPSIS</span></span>
<span data-ttu-id="3e954-103">Disabilita un avviso del log attività e ne imposta i contrassegni.</span><span class="sxs-lookup"><span data-stu-id="3e954-103">Disables an activity log alert and sets its tags.</span></span>

## <span data-ttu-id="3e954-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3e954-104">SYNTAX</span></span>

### <span data-ttu-id="3e954-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3e954-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e954-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="3e954-106">DisableByInputObject</span></span>
```
Disable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e954-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="3e954-107">DisableByResourceId</span></span>
```
Disable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e954-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e954-108">DESCRIPTION</span></span>
<span data-ttu-id="3e954-109">Il cmdlet **Disable-AzActivityLogAlert disattiva** l'avviso e il log delle attività e consente di impostare i relativi contrassegni.</span><span class="sxs-lookup"><span data-stu-id="3e954-109">The **Disable-AzActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="3e954-110">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere la conferma da parte dell'utente prima di applicare la patch alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="3e954-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="3e954-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3e954-111">EXAMPLES</span></span>

### <span data-ttu-id="3e954-112">Esempio 1: disabilitare un avviso del log attività</span><span class="sxs-lookup"><span data-stu-id="3e954-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="3e954-113">Questo comando Disabilita l'avviso del log attività denominato Alert1 nel gruppo di risorse predefinito-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="3e954-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="3e954-114">Questo comando modifica la proprietà Tags dell'avviso del log attività denominato Alert1 e lo Disabilita.</span><span class="sxs-lookup"><span data-stu-id="3e954-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="3e954-115">Esempio 2: disabilitare un avviso del log attività usando un oggetto PSActivityLogAlertResource come input</span><span class="sxs-lookup"><span data-stu-id="3e954-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="3e954-116">Questo comando Disabilita un avviso del log attività denominato Alert1.</span><span class="sxs-lookup"><span data-stu-id="3e954-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="3e954-117">Per questo usa un oggetto PSActivityLogAlertResource come argomento di input.</span><span class="sxs-lookup"><span data-stu-id="3e954-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="3e954-118">Esempio 3: disabilitare il ActivityLogAlert usando il parametro ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e954-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Disable-AzActivityLogAlert
```

<span data-ttu-id="3e954-119">Questo comando Disabilita ActivityLogAlert usando il parametro ResourceId dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="3e954-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="3e954-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3e954-120">PARAMETERS</span></span>

### <span data-ttu-id="3e954-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e954-121">-DefaultProfile</span></span>
<span data-ttu-id="3e954-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3e954-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e954-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e954-123">-InputObject</span></span>
<span data-ttu-id="3e954-124">Imposta la proprietà InputObject tag della chiamata per estrarre il nome necessario, il nome del gruppo di risorse e le proprietà facoltative del tag.</span><span class="sxs-lookup"><span data-stu-id="3e954-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: DisableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e954-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="3e954-125">-Name</span></span>
<span data-ttu-id="3e954-126">Nome dell'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="3e954-126">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e954-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e954-127">-ResourceGroupName</span></span>
<span data-ttu-id="3e954-128">Nome del gruppo di risorse in cui sta per esistere la risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="3e954-128">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e954-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e954-129">-ResourceId</span></span>
<span data-ttu-id="3e954-130">Imposta la proprietà ResourceId tag della chiamata per estrarre le proprietà nome obbligatorio, nome gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="3e954-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e954-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3e954-131">-Confirm</span></span>
<span data-ttu-id="3e954-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e954-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e954-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e954-133">-WhatIf</span></span>
<span data-ttu-id="3e954-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e954-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e954-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3e954-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e954-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e954-136">CommonParameters</span></span>
<span data-ttu-id="3e954-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e954-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e954-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e954-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e954-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3e954-139">INPUTS</span></span>

### <span data-ttu-id="3e954-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3e954-140">System.String</span></span>

### <span data-ttu-id="3e954-141">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="3e954-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="3e954-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3e954-142">OUTPUTS</span></span>

### <span data-ttu-id="3e954-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="3e954-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="3e954-144">Note</span><span class="sxs-lookup"><span data-stu-id="3e954-144">NOTES</span></span>

## <span data-ttu-id="3e954-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3e954-145">RELATED LINKS</span></span>

[<span data-ttu-id="3e954-146">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3e954-146">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="3e954-147">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3e954-147">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="3e954-148">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3e954-148">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="3e954-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="3e954-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="3e954-150">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="3e954-150">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

[<span data-ttu-id="3e954-151">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="3e954-151">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)
