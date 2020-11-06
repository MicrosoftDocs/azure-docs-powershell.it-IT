---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
ms.openlocfilehash: fd232a0f118db5730c41ef1588eaf07d80df69f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508792"
---
# <span data-ttu-id="32064-101">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="32064-101">Remove-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="32064-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32064-102">SYNOPSIS</span></span>
<span data-ttu-id="32064-103">Elimina un abbonamento esistente.</span><span class="sxs-lookup"><span data-stu-id="32064-103">Deletes an existing subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32064-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32064-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32064-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32064-105">DESCRIPTION</span></span>
<span data-ttu-id="32064-106">Il cmdlet **Remove-AzureRmApiManagementSubscription** Elimina un abbonamento esistente.</span><span class="sxs-lookup"><span data-stu-id="32064-106">The **Remove-AzureRmApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="32064-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32064-107">EXAMPLES</span></span>

### <span data-ttu-id="32064-108">Esempio 1: eliminare un abbonamento</span><span class="sxs-lookup"><span data-stu-id="32064-108">Example 1: Delete a subscription</span></span>
```
PS C:\>Remove-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="32064-109">Questo comando Elimina un abbonamento esistente.</span><span class="sxs-lookup"><span data-stu-id="32064-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="32064-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32064-110">PARAMETERS</span></span>

### <span data-ttu-id="32064-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="32064-111">-Context</span></span>
<span data-ttu-id="32064-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="32064-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="32064-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32064-113">-PassThru</span></span>
<span data-ttu-id="32064-114">Indica che questo cmdlet restituisce un valore di $True, se ha esito positivo o un valore di $false, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="32064-114">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

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

### <span data-ttu-id="32064-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="32064-115">-SubscriptionId</span></span>
<span data-ttu-id="32064-116">Specifica l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="32064-116">Specifies the subscription ID.</span></span>

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

### <span data-ttu-id="32064-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="32064-117">-Confirm</span></span>
<span data-ttu-id="32064-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32064-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32064-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32064-119">-WhatIf</span></span>
<span data-ttu-id="32064-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32064-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32064-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32064-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32064-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32064-122">-DefaultProfile</span></span>
<span data-ttu-id="32064-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32064-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32064-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32064-124">CommonParameters</span></span>
<span data-ttu-id="32064-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32064-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32064-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32064-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32064-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32064-127">INPUTS</span></span>

## <span data-ttu-id="32064-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32064-128">OUTPUTS</span></span>

### <span data-ttu-id="32064-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="32064-129">Boolean</span></span>

## <span data-ttu-id="32064-130">Note</span><span class="sxs-lookup"><span data-stu-id="32064-130">NOTES</span></span>

## <span data-ttu-id="32064-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32064-131">RELATED LINKS</span></span>

[<span data-ttu-id="32064-132">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="32064-132">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="32064-133">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="32064-133">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="32064-134">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="32064-134">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


