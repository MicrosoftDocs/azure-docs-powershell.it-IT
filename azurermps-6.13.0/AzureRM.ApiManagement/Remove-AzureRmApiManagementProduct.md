---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProduct.md
ms.openlocfilehash: 61a4ab9e7a827cffce861cc9ebaf7382e16e8fcb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685792"
---
# <span data-ttu-id="6499d-101">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="6499d-101">Remove-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="6499d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6499d-102">SYNOPSIS</span></span>
<span data-ttu-id="6499d-103">Rimuove un prodotto di gestione API esistente.</span><span class="sxs-lookup"><span data-stu-id="6499d-103">Removes an existing API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6499d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6499d-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6499d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6499d-105">DESCRIPTION</span></span>
<span data-ttu-id="6499d-106">Il cmdlet **Remove-AzureRmApiManagementProduct** rimuove un prodotto di gestione API esistente.</span><span class="sxs-lookup"><span data-stu-id="6499d-106">The **Remove-AzureRmApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="6499d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6499d-107">EXAMPLES</span></span>

### <span data-ttu-id="6499d-108">Esempio 1: rimuovere un prodotto esistente e tutti gli abbonamenti</span><span class="sxs-lookup"><span data-stu-id="6499d-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProduct -Context $apimContext -Id "0123456789" -DeleteSubscriptions -Force
```

<span data-ttu-id="6499d-109">Questo comando rimuove un prodotto esistente e tutti gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="6499d-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="6499d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6499d-110">PARAMETERS</span></span>

### <span data-ttu-id="6499d-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="6499d-111">-Context</span></span>
<span data-ttu-id="6499d-112">Specifica un'istanza dell'oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="6499d-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6499d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6499d-113">-DefaultProfile</span></span>
<span data-ttu-id="6499d-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6499d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6499d-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="6499d-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="6499d-116">Indica se eliminare gli abbonamenti al prodotto.</span><span class="sxs-lookup"><span data-stu-id="6499d-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="6499d-117">Se non si imposta questo parametro e non esiste una sottoscrizione, viene generata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="6499d-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="6499d-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6499d-118">-PassThru</span></span>
<span data-ttu-id="6499d-119">Indica che questo cmdlet restituisce un valore di $True, se ha esito positivo o un valore di $False, se non riesce.</span><span class="sxs-lookup"><span data-stu-id="6499d-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="6499d-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="6499d-120">-ProductId</span></span>
<span data-ttu-id="6499d-121">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="6499d-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="6499d-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6499d-122">-Confirm</span></span>
<span data-ttu-id="6499d-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6499d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6499d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6499d-124">-WhatIf</span></span>
<span data-ttu-id="6499d-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6499d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6499d-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6499d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6499d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6499d-127">CommonParameters</span></span>
<span data-ttu-id="6499d-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6499d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6499d-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6499d-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6499d-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6499d-130">INPUTS</span></span>

### <span data-ttu-id="6499d-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6499d-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6499d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6499d-132">System.String</span></span>

### <span data-ttu-id="6499d-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6499d-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6499d-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6499d-134">OUTPUTS</span></span>

### <span data-ttu-id="6499d-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6499d-135">System.Boolean</span></span>

## <span data-ttu-id="6499d-136">Note</span><span class="sxs-lookup"><span data-stu-id="6499d-136">NOTES</span></span>

## <span data-ttu-id="6499d-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6499d-137">RELATED LINKS</span></span>

[<span data-ttu-id="6499d-138">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="6499d-138">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="6499d-139">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="6499d-139">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="6499d-140">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="6499d-140">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


