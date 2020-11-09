---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 33b00df9e0c9c5b5e0ef04d22b745942535effcb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302190"
---
# <span data-ttu-id="0bd3a-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="0bd3a-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="0bd3a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0bd3a-102">SYNOPSIS</span></span>
<span data-ttu-id="0bd3a-103">Rimuove un prodotto di gestione API esistente.</span><span class="sxs-lookup"><span data-stu-id="0bd3a-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="0bd3a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0bd3a-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bd3a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0bd3a-105">DESCRIPTION</span></span>
<span data-ttu-id="0bd3a-106">Il cmdlet **Remove-AzApiManagementProduct** rimuove un prodotto di gestione API esistente.</span><span class="sxs-lookup"><span data-stu-id="0bd3a-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="0bd3a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0bd3a-107">EXAMPLES</span></span>

### <span data-ttu-id="0bd3a-108">Esempio 1: rimuovere un prodotto esistente e tutti gli abbonamenti</span><span class="sxs-lookup"><span data-stu-id="0bd3a-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="0bd3a-109">Questo comando rimuove un prodotto esistente e tutti gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="0bd3a-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="0bd3a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0bd3a-110">PARAMETERS</span></span>

### <span data-ttu-id="0bd3a-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="0bd3a-111">-Context</span></span>
<span data-ttu-id="0bd3a-112">Specifica un'istanza dell'oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="0bd3a-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="0bd3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bd3a-113">-DefaultProfile</span></span>
<span data-ttu-id="0bd3a-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0bd3a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bd3a-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="0bd3a-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="0bd3a-116">Indica se eliminare gli abbonamenti al prodotto.</span><span class="sxs-lookup"><span data-stu-id="0bd3a-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="0bd3a-117">Se non si imposta questo parametro e non esiste una sottoscrizione, viene generata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="0bd3a-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="0bd3a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bd3a-118">-PassThru</span></span>
<span data-ttu-id="0bd3a-119">Indica che questo cmdlet restituisce un valore di $True, se ha esito positivo o un valore di $False, se non riesce.</span><span class="sxs-lookup"><span data-stu-id="0bd3a-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="0bd3a-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="0bd3a-120">-ProductId</span></span>
<span data-ttu-id="0bd3a-121">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="0bd3a-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="0bd3a-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0bd3a-122">-Confirm</span></span>
<span data-ttu-id="0bd3a-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0bd3a-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bd3a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bd3a-124">-WhatIf</span></span>
<span data-ttu-id="0bd3a-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0bd3a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bd3a-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0bd3a-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bd3a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bd3a-127">CommonParameters</span></span>
<span data-ttu-id="0bd3a-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bd3a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bd3a-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0bd3a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bd3a-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0bd3a-130">INPUTS</span></span>

### <span data-ttu-id="0bd3a-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0bd3a-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0bd3a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0bd3a-132">System.String</span></span>

### <span data-ttu-id="0bd3a-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0bd3a-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0bd3a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0bd3a-134">OUTPUTS</span></span>

### <span data-ttu-id="0bd3a-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0bd3a-135">System.Boolean</span></span>

## <span data-ttu-id="0bd3a-136">Note</span><span class="sxs-lookup"><span data-stu-id="0bd3a-136">NOTES</span></span>

## <span data-ttu-id="0bd3a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0bd3a-137">RELATED LINKS</span></span>

[<span data-ttu-id="0bd3a-138">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="0bd3a-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="0bd3a-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="0bd3a-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="0bd3a-140">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="0bd3a-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


