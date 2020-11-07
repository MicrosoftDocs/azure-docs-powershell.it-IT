---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 72dbe137fd783cb8941fe27e6883bd0ed8e08206
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852453"
---
# <span data-ttu-id="38d8e-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="38d8e-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="38d8e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38d8e-102">SYNOPSIS</span></span>
<span data-ttu-id="38d8e-103">Rimuove un prodotto di gestione API esistente.</span><span class="sxs-lookup"><span data-stu-id="38d8e-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="38d8e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38d8e-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38d8e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38d8e-105">DESCRIPTION</span></span>
<span data-ttu-id="38d8e-106">Il cmdlet **Remove-AzApiManagementProduct** rimuove un prodotto di gestione API esistente.</span><span class="sxs-lookup"><span data-stu-id="38d8e-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="38d8e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38d8e-107">EXAMPLES</span></span>

### <span data-ttu-id="38d8e-108">Esempio 1: rimuovere un prodotto esistente e tutti gli abbonamenti</span><span class="sxs-lookup"><span data-stu-id="38d8e-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="38d8e-109">Questo comando rimuove un prodotto esistente e tutti gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="38d8e-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="38d8e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38d8e-110">PARAMETERS</span></span>

### <span data-ttu-id="38d8e-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="38d8e-111">-Context</span></span>
<span data-ttu-id="38d8e-112">Specifica un'istanza dell'oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="38d8e-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="38d8e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d8e-113">-DefaultProfile</span></span>
<span data-ttu-id="38d8e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38d8e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38d8e-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="38d8e-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="38d8e-116">Indica se eliminare gli abbonamenti al prodotto.</span><span class="sxs-lookup"><span data-stu-id="38d8e-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="38d8e-117">Se non si imposta questo parametro e non esiste una sottoscrizione, viene generata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="38d8e-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="38d8e-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38d8e-118">-PassThru</span></span>
<span data-ttu-id="38d8e-119">Indica che questo cmdlet restituisce un valore di $True, se ha esito positivo o un valore di $False, se non riesce.</span><span class="sxs-lookup"><span data-stu-id="38d8e-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="38d8e-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="38d8e-120">-ProductId</span></span>
<span data-ttu-id="38d8e-121">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="38d8e-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="38d8e-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="38d8e-122">-Confirm</span></span>
<span data-ttu-id="38d8e-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38d8e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38d8e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38d8e-124">-WhatIf</span></span>
<span data-ttu-id="38d8e-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38d8e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38d8e-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38d8e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38d8e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d8e-127">CommonParameters</span></span>
<span data-ttu-id="38d8e-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38d8e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d8e-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38d8e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d8e-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38d8e-130">INPUTS</span></span>

### <span data-ttu-id="38d8e-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="38d8e-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="38d8e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="38d8e-132">System.String</span></span>

### <span data-ttu-id="38d8e-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="38d8e-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="38d8e-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38d8e-134">OUTPUTS</span></span>

### <span data-ttu-id="38d8e-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="38d8e-135">System.Boolean</span></span>

## <span data-ttu-id="38d8e-136">Note</span><span class="sxs-lookup"><span data-stu-id="38d8e-136">NOTES</span></span>

## <span data-ttu-id="38d8e-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38d8e-137">RELATED LINKS</span></span>

[<span data-ttu-id="38d8e-138">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="38d8e-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="38d8e-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="38d8e-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="38d8e-140">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="38d8e-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


