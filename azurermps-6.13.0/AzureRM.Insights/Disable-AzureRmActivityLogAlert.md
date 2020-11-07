---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/disable-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
ms.openlocfilehash: 42107266ba38dff03c77336f14015853ef9b56c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686187"
---
# <span data-ttu-id="69ad7-101">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="69ad7-101">Disable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="69ad7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69ad7-102">SYNOPSIS</span></span>
<span data-ttu-id="69ad7-103">Disabilita un avviso del log attività e ne imposta i contrassegni.</span><span class="sxs-lookup"><span data-stu-id="69ad7-103">Disables an activity log alert and sets its tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69ad7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69ad7-104">SYNTAX</span></span>

### <span data-ttu-id="69ad7-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="69ad7-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69ad7-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="69ad7-106">DisableByInputObject</span></span>
```
Disable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69ad7-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="69ad7-107">DisableByResourceId</span></span>
```
Disable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69ad7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69ad7-108">DESCRIPTION</span></span>
<span data-ttu-id="69ad7-109">Il cmdlet **Disable-AzureRmActivityLogAlert disattiva** l'avviso e il log delle attività e consente di impostare i relativi contrassegni.</span><span class="sxs-lookup"><span data-stu-id="69ad7-109">The **Disable-AzureRmActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="69ad7-110">Questo cmdlet implementa il modello ShouldProcess, vale a dire che potrebbe richiedere la conferma da parte dell'utente prima di applicare la patch alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="69ad7-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="69ad7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69ad7-111">EXAMPLES</span></span>

### <span data-ttu-id="69ad7-112">Esempio 1: disabilitare un avviso del log attività</span><span class="sxs-lookup"><span data-stu-id="69ad7-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="69ad7-113">Questo comando Disabilita l'avviso del log attività denominato Alert1 nel gruppo di risorse predefinito-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="69ad7-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="69ad7-114">Questo comando modifica la proprietà Tags dell'avviso del log attività denominato Alert1 e lo Disabilita.</span><span class="sxs-lookup"><span data-stu-id="69ad7-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="69ad7-115">Esempio 2: disabilitare un avviso del log attività usando un oggetto PSActivityLogAlertResource come input</span><span class="sxs-lookup"><span data-stu-id="69ad7-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="69ad7-116">Questo comando Disabilita un avviso del log attività denominato Alert1.</span><span class="sxs-lookup"><span data-stu-id="69ad7-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="69ad7-117">Per questo usa un oggetto PSActivityLogAlertResource come argomento di input.</span><span class="sxs-lookup"><span data-stu-id="69ad7-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="69ad7-118">Esempio 3: disabilitare il ActivityLogAlert usando il parametro ResourceId</span><span class="sxs-lookup"><span data-stu-id="69ad7-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Disable-AzureRmActivityLogAlert
```

<span data-ttu-id="69ad7-119">Questo comando Disabilita ActivityLogAlert usando il parametro ResourceId dalla pipe.</span><span class="sxs-lookup"><span data-stu-id="69ad7-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="69ad7-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69ad7-120">PARAMETERS</span></span>

### <span data-ttu-id="69ad7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69ad7-121">-DefaultProfile</span></span>
<span data-ttu-id="69ad7-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="69ad7-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69ad7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69ad7-123">-InputObject</span></span>
<span data-ttu-id="69ad7-124">Imposta la proprietà InputObject tag della chiamata per estrarre il nome necessario, il nome del gruppo di risorse e le proprietà facoltative del tag.</span><span class="sxs-lookup"><span data-stu-id="69ad7-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

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

### <span data-ttu-id="69ad7-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="69ad7-125">-Name</span></span>
<span data-ttu-id="69ad7-126">Nome dell'avviso del log attività.</span><span class="sxs-lookup"><span data-stu-id="69ad7-126">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="69ad7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69ad7-127">-ResourceGroupName</span></span>
<span data-ttu-id="69ad7-128">Nome del gruppo di risorse in cui sta per esistere la risorsa di avviso.</span><span class="sxs-lookup"><span data-stu-id="69ad7-128">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="69ad7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69ad7-129">-ResourceId</span></span>
<span data-ttu-id="69ad7-130">Imposta la proprietà ResourceId tag della chiamata per estrarre le proprietà nome obbligatorio, nome gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="69ad7-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="69ad7-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="69ad7-131">-Confirm</span></span>
<span data-ttu-id="69ad7-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69ad7-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69ad7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69ad7-133">-WhatIf</span></span>
<span data-ttu-id="69ad7-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69ad7-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69ad7-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69ad7-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69ad7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69ad7-136">CommonParameters</span></span>
<span data-ttu-id="69ad7-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69ad7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69ad7-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69ad7-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69ad7-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69ad7-139">INPUTS</span></span>

### <span data-ttu-id="69ad7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="69ad7-140">System.String</span></span>

### <span data-ttu-id="69ad7-141">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="69ad7-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="69ad7-142">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="69ad7-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="69ad7-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69ad7-143">OUTPUTS</span></span>

### <span data-ttu-id="69ad7-144">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="69ad7-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="69ad7-145">Note</span><span class="sxs-lookup"><span data-stu-id="69ad7-145">NOTES</span></span>

## <span data-ttu-id="69ad7-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69ad7-146">RELATED LINKS</span></span>

[<span data-ttu-id="69ad7-147">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="69ad7-147">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="69ad7-148">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="69ad7-148">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="69ad7-149">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="69ad7-149">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="69ad7-150">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="69ad7-150">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="69ad7-151">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="69ad7-151">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="69ad7-152">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="69ad7-152">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)
