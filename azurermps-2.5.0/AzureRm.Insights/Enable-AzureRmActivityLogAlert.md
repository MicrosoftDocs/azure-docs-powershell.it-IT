---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/enable-azurermactivitylogalert
schema: 2.0.0
ms.openlocfilehash: 856e3abc5cf99c7ae7f871619476717af21aed9a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867111"
---
# <span data-ttu-id="b300c-101">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b300c-101">Enable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="b300c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b300c-102">SYNOPSIS</span></span>
<span data-ttu-id="b300c-103">Abilita un avviso del log attività e ne imposta i contrassegni.</span><span class="sxs-lookup"><span data-stu-id="b300c-103">Enables an activity log alert and sets its Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b300c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b300c-104">SYNTAX</span></span>

### <span data-ttu-id="b300c-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b300c-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b300c-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="b300c-106">EnableByInputObject</span></span>
```
Enable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b300c-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="b300c-107">EnableByResourceId</span></span>
```
Enable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b300c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b300c-108">DESCRIPTION</span></span>
<span data-ttu-id="b300c-109">Il cmdlet **Enable-AzureRmActivityLogAlert** consente di abilitare un avviso del log attività e di impostarne i contrassegni.</span><span class="sxs-lookup"><span data-stu-id="b300c-109">The **Enable-AzureRmActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="b300c-110">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere la conferma da parte dell'utente prima di applicare la patch alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="b300c-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="b300c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b300c-111">EXAMPLES</span></span>

### <span data-ttu-id="b300c-112">Esempio 1: disabilitare un avviso del log attività</span><span class="sxs-lookup"><span data-stu-id="b300c-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Enable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="b300c-113">Questo comando Abilita l'avviso del log attività denominato Alert1 nel gruppo di risorse predefinito-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="b300c-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="b300c-114">Esempio 2: abilitare un avviso del log attività usando un oggetto PSActivityLogAlertResource come input</span><span class="sxs-lookup"><span data-stu-id="b300c-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="b300c-115">Questo comando Abilita l'avviso di un log attività denominato Alert1.</span><span class="sxs-lookup"><span data-stu-id="b300c-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="b300c-116">Per questo usa un oggetto PSActivityLogAlertResource come argomento di input.</span><span class="sxs-lookup"><span data-stu-id="b300c-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="b300c-117">Esempio 3: abilitare il ActivityLogAlert usando il parametro ResourceId</span><span class="sxs-lookup"><span data-stu-id="b300c-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Enable-AzureRmActivityLogAlert
```

<span data-ttu-id="b300c-118">Questo comando consente a ActivityLogAlert di usare il parametro ResourceId dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="b300c-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="b300c-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b300c-119">PARAMETERS</span></span>

### <span data-ttu-id="b300c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b300c-120">-DefaultProfile</span></span>
<span data-ttu-id="b300c-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b300c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b300c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b300c-122">-InputObject</span></span>
<span data-ttu-id="b300c-123">Imposta la proprietà Tag InputObject della chiamata per estrarre il nome necessario, il nome del gruppo di risorse e le proprietà facoltative dei tag.</span><span class="sxs-lookup"><span data-stu-id="b300c-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

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

### <span data-ttu-id="b300c-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="b300c-124">-Name</span></span>
<span data-ttu-id="b300c-125">Nome dell'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="b300c-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="b300c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b300c-126">-ResourceGroupName</span></span>
<span data-ttu-id="b300c-127">Nome del gruppo di risorse in cui sta per esistere la risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="b300c-127">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="b300c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b300c-128">-ResourceId</span></span>
<span data-ttu-id="b300c-129">Imposta la proprietà ResourceId tag della chiamata per estrarre le proprietà nome obbligatorio, nome gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="b300c-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="b300c-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b300c-130">-Confirm</span></span>
<span data-ttu-id="b300c-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b300c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b300c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b300c-132">-WhatIf</span></span>
<span data-ttu-id="b300c-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b300c-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b300c-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b300c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b300c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b300c-135">CommonParameters</span></span>
<span data-ttu-id="b300c-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b300c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b300c-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b300c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b300c-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b300c-138">INPUTS</span></span>

### <span data-ttu-id="b300c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b300c-139">System.String</span></span>

### <span data-ttu-id="b300c-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="b300c-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="b300c-141">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b300c-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="b300c-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b300c-142">OUTPUTS</span></span>

### <span data-ttu-id="b300c-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="b300c-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="b300c-144">Note</span><span class="sxs-lookup"><span data-stu-id="b300c-144">NOTES</span></span>

## <span data-ttu-id="b300c-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b300c-145">RELATED LINKS</span></span>

[<span data-ttu-id="b300c-146">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b300c-146">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="b300c-147">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b300c-147">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="b300c-148">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b300c-148">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="b300c-149">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="b300c-149">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="b300c-150">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="b300c-150">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="b300c-151">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b300c-151">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)
