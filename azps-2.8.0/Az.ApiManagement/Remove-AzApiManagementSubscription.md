---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 5d3ad3481a57f2578678daa88c1f3e87e9893f7c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675923"
---
# <span data-ttu-id="2a0da-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2a0da-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="2a0da-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2a0da-102">SYNOPSIS</span></span>
<span data-ttu-id="2a0da-103">Elimina un abbonamento esistente.</span><span class="sxs-lookup"><span data-stu-id="2a0da-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="2a0da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a0da-104">SYNTAX</span></span>

### <span data-ttu-id="2a0da-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2a0da-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a0da-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2a0da-106">ByInputObject</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -InputObject <PsApiManagementSubscription> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a0da-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2a0da-107">ByResourceId</span></span>
```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String>
 -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a0da-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a0da-108">DESCRIPTION</span></span>
<span data-ttu-id="2a0da-109">Il cmdlet **Remove-AzApiManagementSubscription** Elimina un abbonamento esistente.</span><span class="sxs-lookup"><span data-stu-id="2a0da-109">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="2a0da-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a0da-110">EXAMPLES</span></span>

### <span data-ttu-id="2a0da-111">Esempio 1: eliminare un abbonamento</span><span class="sxs-lookup"><span data-stu-id="2a0da-111">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="2a0da-112">Questo comando Elimina un abbonamento esistente.</span><span class="sxs-lookup"><span data-stu-id="2a0da-112">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="2a0da-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a0da-113">PARAMETERS</span></span>

### <span data-ttu-id="2a0da-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="2a0da-114">-Context</span></span>
<span data-ttu-id="2a0da-115">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2a0da-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a0da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a0da-116">-DefaultProfile</span></span>
<span data-ttu-id="2a0da-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a0da-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a0da-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a0da-118">-InputObject</span></span>
<span data-ttu-id="2a0da-119">Istanza di PsApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="2a0da-119">Instance of PsApiManagementSubscription.</span></span> <span data-ttu-id="2a0da-120">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2a0da-120">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a0da-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a0da-121">-PassThru</span></span>
<span data-ttu-id="2a0da-122">Indica che questo cmdlet restituisce un valore di $True, se ha esito positivo o un valore di $false, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2a0da-122">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a0da-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a0da-123">-ResourceId</span></span>
<span data-ttu-id="2a0da-124">ARM ResourceId dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="2a0da-124">Arm ResourceId of Subscription.</span></span> <span data-ttu-id="2a0da-125">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2a0da-125">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a0da-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2a0da-126">-SubscriptionId</span></span>
<span data-ttu-id="2a0da-127">Specifica l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="2a0da-127">Specifies the subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a0da-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2a0da-128">-Confirm</span></span>
<span data-ttu-id="2a0da-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a0da-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a0da-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a0da-130">-WhatIf</span></span>
<span data-ttu-id="2a0da-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a0da-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a0da-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a0da-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a0da-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a0da-133">CommonParameters</span></span>
<span data-ttu-id="2a0da-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a0da-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a0da-135">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a0da-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a0da-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2a0da-136">INPUTS</span></span>

### <span data-ttu-id="2a0da-137">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2a0da-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2a0da-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2a0da-138">System.String</span></span>

### <span data-ttu-id="2a0da-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2a0da-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2a0da-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a0da-140">OUTPUTS</span></span>

### <span data-ttu-id="2a0da-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2a0da-141">System.Boolean</span></span>

## <span data-ttu-id="2a0da-142">Note</span><span class="sxs-lookup"><span data-stu-id="2a0da-142">NOTES</span></span>

## <span data-ttu-id="2a0da-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a0da-143">RELATED LINKS</span></span>

[<span data-ttu-id="2a0da-144">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2a0da-144">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="2a0da-145">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2a0da-145">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="2a0da-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2a0da-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


