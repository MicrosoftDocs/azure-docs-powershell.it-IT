---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementSubscription.md
ms.openlocfilehash: 411fa67d81b772c2e9dcd6b1690e8eac50de3ea0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852434"
---
# <span data-ttu-id="7b0f1-101">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7b0f1-101">Remove-AzApiManagementSubscription</span></span>

## <span data-ttu-id="7b0f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7b0f1-102">SYNOPSIS</span></span>
<span data-ttu-id="7b0f1-103">Elimina un abbonamento esistente.</span><span class="sxs-lookup"><span data-stu-id="7b0f1-103">Deletes an existing subscription.</span></span>

## <span data-ttu-id="7b0f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b0f1-104">SYNTAX</span></span>

```
Remove-AzApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b0f1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b0f1-105">DESCRIPTION</span></span>
<span data-ttu-id="7b0f1-106">Il cmdlet **Remove-AzApiManagementSubscription** Elimina un abbonamento esistente.</span><span class="sxs-lookup"><span data-stu-id="7b0f1-106">The **Remove-AzApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="7b0f1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b0f1-107">EXAMPLES</span></span>

### <span data-ttu-id="7b0f1-108">Esempio 1: eliminare un abbonamento</span><span class="sxs-lookup"><span data-stu-id="7b0f1-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="7b0f1-109">Questo comando Elimina un abbonamento esistente.</span><span class="sxs-lookup"><span data-stu-id="7b0f1-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="7b0f1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7b0f1-110">PARAMETERS</span></span>

### <span data-ttu-id="7b0f1-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="7b0f1-111">-Context</span></span>
<span data-ttu-id="7b0f1-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7b0f1-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b0f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b0f1-113">-DefaultProfile</span></span>
<span data-ttu-id="7b0f1-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b0f1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b0f1-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b0f1-115">-PassThru</span></span>
<span data-ttu-id="7b0f1-116">Indica che questo cmdlet restituisce un valore di $True, se ha esito positivo o un valore di $false, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="7b0f1-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="7b0f1-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7b0f1-117">-SubscriptionId</span></span>
<span data-ttu-id="7b0f1-118">Specifica l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="7b0f1-118">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="7b0f1-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7b0f1-119">-Confirm</span></span>
<span data-ttu-id="7b0f1-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b0f1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b0f1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b0f1-121">-WhatIf</span></span>
<span data-ttu-id="7b0f1-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b0f1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b0f1-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b0f1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b0f1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b0f1-124">CommonParameters</span></span>
<span data-ttu-id="7b0f1-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b0f1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b0f1-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b0f1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b0f1-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7b0f1-127">INPUTS</span></span>

### <span data-ttu-id="7b0f1-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7b0f1-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7b0f1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7b0f1-129">System.String</span></span>

### <span data-ttu-id="7b0f1-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7b0f1-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7b0f1-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b0f1-131">OUTPUTS</span></span>

### <span data-ttu-id="7b0f1-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7b0f1-132">System.Boolean</span></span>

## <span data-ttu-id="7b0f1-133">Note</span><span class="sxs-lookup"><span data-stu-id="7b0f1-133">NOTES</span></span>

## <span data-ttu-id="7b0f1-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b0f1-134">RELATED LINKS</span></span>

[<span data-ttu-id="7b0f1-135">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7b0f1-135">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="7b0f1-136">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7b0f1-136">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="7b0f1-137">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="7b0f1-137">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


