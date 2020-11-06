---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
ms.openlocfilehash: 5c5bd7d0b7df385645bdb51d684616f2c0d7eaa5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508435"
---
# <span data-ttu-id="38f2f-101">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="38f2f-101">Remove-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="38f2f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38f2f-102">SYNOPSIS</span></span>
<span data-ttu-id="38f2f-103">Rimuove un prodotto di gestione API esistente.</span><span class="sxs-lookup"><span data-stu-id="38f2f-103">Removes an existing API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38f2f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38f2f-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38f2f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38f2f-105">DESCRIPTION</span></span>
<span data-ttu-id="38f2f-106">Il cmdlet **Remove-AzureRmApiManagementProduct** rimuove un prodotto di gestione API esistente.</span><span class="sxs-lookup"><span data-stu-id="38f2f-106">The **Remove-AzureRmApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="38f2f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38f2f-107">EXAMPLES</span></span>

### <span data-ttu-id="38f2f-108">Esempio 1: rimuovere un prodotto esistente e tutti gli abbonamenti</span><span class="sxs-lookup"><span data-stu-id="38f2f-108">Example 1: Remove an existing product and all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProduct -Context $apimContext -Id "0123456789" -DeleteSubscriptions -Force
```

<span data-ttu-id="38f2f-109">Questo comando rimuove un prodotto esistente e tutti gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="38f2f-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="38f2f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38f2f-110">PARAMETERS</span></span>

### <span data-ttu-id="38f2f-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="38f2f-111">-Context</span></span>
<span data-ttu-id="38f2f-112">Specifica un'istanza dell'oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="38f2f-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="38f2f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38f2f-113">-DefaultProfile</span></span>
<span data-ttu-id="38f2f-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38f2f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="38f2f-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="38f2f-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="38f2f-116">Indica se eliminare gli abbonamenti al prodotto.</span><span class="sxs-lookup"><span data-stu-id="38f2f-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="38f2f-117">Se non si imposta questo parametro e non esiste una sottoscrizione, viene generata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="38f2f-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="38f2f-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38f2f-118">-PassThru</span></span>
<span data-ttu-id="38f2f-119">Indica che questo cmdlet restituisce un valore di $True, se ha esito positivo o un valore di $False, se non riesce.</span><span class="sxs-lookup"><span data-stu-id="38f2f-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="38f2f-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="38f2f-120">-ProductId</span></span>
<span data-ttu-id="38f2f-121">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="38f2f-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="38f2f-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="38f2f-122">-Confirm</span></span>
<span data-ttu-id="38f2f-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38f2f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38f2f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38f2f-124">-WhatIf</span></span>
<span data-ttu-id="38f2f-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38f2f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38f2f-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38f2f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38f2f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f2f-127">CommonParameters</span></span>
<span data-ttu-id="38f2f-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38f2f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f2f-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38f2f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f2f-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38f2f-130">INPUTS</span></span>

### <span data-ttu-id="38f2f-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="38f2f-131">None</span></span>
<span data-ttu-id="38f2f-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="38f2f-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="38f2f-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38f2f-133">OUTPUTS</span></span>

### <span data-ttu-id="38f2f-134">bool</span><span class="sxs-lookup"><span data-stu-id="38f2f-134">bool</span></span>

## <span data-ttu-id="38f2f-135">Note</span><span class="sxs-lookup"><span data-stu-id="38f2f-135">NOTES</span></span>

## <span data-ttu-id="38f2f-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38f2f-136">RELATED LINKS</span></span>

[<span data-ttu-id="38f2f-137">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="38f2f-137">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="38f2f-138">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="38f2f-138">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="38f2f-139">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="38f2f-139">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


