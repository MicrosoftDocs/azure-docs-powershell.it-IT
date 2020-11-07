---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 09a0af4685701de60fc85c1572b492e7582ff71e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686968"
---
# <span data-ttu-id="a2d81-101">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a2d81-101">Remove-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="a2d81-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a2d81-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d81-103">Elimina un abbonamento esistente.</span><span class="sxs-lookup"><span data-stu-id="a2d81-103">Deletes an existing subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2d81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2d81-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2d81-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2d81-105">DESCRIPTION</span></span>
<span data-ttu-id="a2d81-106">Il cmdlet **Remove-AzureRmApiManagementSubscription** Elimina un abbonamento esistente.</span><span class="sxs-lookup"><span data-stu-id="a2d81-106">The **Remove-AzureRmApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="a2d81-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2d81-107">EXAMPLES</span></span>

### <span data-ttu-id="a2d81-108">Esempio 1: eliminare un abbonamento</span><span class="sxs-lookup"><span data-stu-id="a2d81-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="a2d81-109">Questo comando Elimina un abbonamento esistente.</span><span class="sxs-lookup"><span data-stu-id="a2d81-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="a2d81-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a2d81-110">PARAMETERS</span></span>

### <span data-ttu-id="a2d81-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="a2d81-111">-Context</span></span>
<span data-ttu-id="a2d81-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="a2d81-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a2d81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d81-113">-DefaultProfile</span></span>
<span data-ttu-id="a2d81-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a2d81-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2d81-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a2d81-115">-PassThru</span></span>
<span data-ttu-id="a2d81-116">Indica che questo cmdlet restituisce un valore di $True, se ha esito positivo o un valore di $false, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a2d81-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="a2d81-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a2d81-117">-SubscriptionId</span></span>
<span data-ttu-id="a2d81-118">Specifica l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a2d81-118">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="a2d81-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a2d81-119">-Confirm</span></span>
<span data-ttu-id="a2d81-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2d81-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2d81-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2d81-121">-WhatIf</span></span>
<span data-ttu-id="a2d81-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2d81-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2d81-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a2d81-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2d81-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d81-124">CommonParameters</span></span>
<span data-ttu-id="a2d81-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2d81-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d81-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2d81-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d81-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a2d81-127">INPUTS</span></span>

### <span data-ttu-id="a2d81-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a2d81-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a2d81-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a2d81-129">System.String</span></span>

### <span data-ttu-id="a2d81-130">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a2d81-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a2d81-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2d81-131">OUTPUTS</span></span>

### <span data-ttu-id="a2d81-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a2d81-132">System.Boolean</span></span>

## <span data-ttu-id="a2d81-133">Note</span><span class="sxs-lookup"><span data-stu-id="a2d81-133">NOTES</span></span>

## <span data-ttu-id="a2d81-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2d81-134">RELATED LINKS</span></span>

[<span data-ttu-id="a2d81-135">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a2d81-135">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="a2d81-136">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a2d81-136">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="a2d81-137">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="a2d81-137">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


