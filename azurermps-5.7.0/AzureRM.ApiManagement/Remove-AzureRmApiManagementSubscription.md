---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 329EF130-5CC9-4BFF-8561-DE5274018B09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 777d71dec17f75cba84c15c7499e5ec56ffb854a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688587"
---
# <span data-ttu-id="ee05b-101">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ee05b-101">Remove-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="ee05b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee05b-102">SYNOPSIS</span></span>
<span data-ttu-id="ee05b-103">Elimina un abbonamento esistente.</span><span class="sxs-lookup"><span data-stu-id="ee05b-103">Deletes an existing subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee05b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee05b-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementSubscription -Context <PsApiManagementContext> -SubscriptionId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee05b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee05b-105">DESCRIPTION</span></span>
<span data-ttu-id="ee05b-106">Il cmdlet **Remove-AzureRmApiManagementSubscription** Elimina un abbonamento esistente.</span><span class="sxs-lookup"><span data-stu-id="ee05b-106">The **Remove-AzureRmApiManagementSubscription** cmdlet deletes an existing subscription.</span></span>

## <span data-ttu-id="ee05b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee05b-107">EXAMPLES</span></span>

### <span data-ttu-id="ee05b-108">Esempio 1: eliminare un abbonamento</span><span class="sxs-lookup"><span data-stu-id="ee05b-108">Example 1: Delete a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789" -Force
```

<span data-ttu-id="ee05b-109">Questo comando Elimina un abbonamento esistente.</span><span class="sxs-lookup"><span data-stu-id="ee05b-109">This command deletes an existing subscription.</span></span>

## <span data-ttu-id="ee05b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee05b-110">PARAMETERS</span></span>

### <span data-ttu-id="ee05b-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="ee05b-111">-Context</span></span>
<span data-ttu-id="ee05b-112">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ee05b-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee05b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee05b-113">-DefaultProfile</span></span>
<span data-ttu-id="ee05b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee05b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="ee05b-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee05b-115">-PassThru</span></span>
<span data-ttu-id="ee05b-116">Indica che questo cmdlet restituisce un valore di $True, se ha esito positivo o un valore di $false, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ee05b-116">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $false, otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee05b-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee05b-117">-SubscriptionId</span></span>
<span data-ttu-id="ee05b-118">Specifica l'ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ee05b-118">Specifies the subscription ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee05b-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ee05b-119">-Confirm</span></span>
<span data-ttu-id="ee05b-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee05b-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee05b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee05b-121">-WhatIf</span></span>
<span data-ttu-id="ee05b-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee05b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee05b-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee05b-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee05b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee05b-124">CommonParameters</span></span>
<span data-ttu-id="ee05b-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee05b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee05b-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee05b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee05b-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee05b-127">INPUTS</span></span>

### <span data-ttu-id="ee05b-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ee05b-128">None</span></span>
<span data-ttu-id="ee05b-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="ee05b-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ee05b-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee05b-130">OUTPUTS</span></span>

### <span data-ttu-id="ee05b-131">Boolean</span><span class="sxs-lookup"><span data-stu-id="ee05b-131">Boolean</span></span>

## <span data-ttu-id="ee05b-132">Note</span><span class="sxs-lookup"><span data-stu-id="ee05b-132">NOTES</span></span>

## <span data-ttu-id="ee05b-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee05b-133">RELATED LINKS</span></span>

[<span data-ttu-id="ee05b-134">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ee05b-134">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="ee05b-135">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ee05b-135">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="ee05b-136">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ee05b-136">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


