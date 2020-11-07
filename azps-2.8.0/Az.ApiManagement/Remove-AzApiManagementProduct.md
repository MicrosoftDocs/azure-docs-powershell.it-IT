---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 03bc30ddfcf1543b54466dc388c70ceba330d4ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675932"
---
# <span data-ttu-id="50ec9-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="50ec9-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="50ec9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="50ec9-103">Rimuove un prodotto di gestione API esistente.</span><span class="sxs-lookup"><span data-stu-id="50ec9-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="50ec9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50ec9-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50ec9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50ec9-105">DESCRIPTION</span></span>
<span data-ttu-id="50ec9-106">Il cmdlet **Remove-AzApiManagementProduct** rimuove un prodotto di gestione API esistente.</span><span class="sxs-lookup"><span data-stu-id="50ec9-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="50ec9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50ec9-107">EXAMPLES</span></span>

### <span data-ttu-id="50ec9-108">Esempio 1: rimuovere un prodotto esistente e tutti gli abbonamenti</span><span class="sxs-lookup"><span data-stu-id="50ec9-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="50ec9-109">Questo comando rimuove un prodotto esistente e tutti gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="50ec9-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="50ec9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50ec9-110">PARAMETERS</span></span>

### <span data-ttu-id="50ec9-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="50ec9-111">-Context</span></span>
<span data-ttu-id="50ec9-112">Specifica un'istanza dell'oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="50ec9-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="50ec9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50ec9-113">-DefaultProfile</span></span>
<span data-ttu-id="50ec9-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50ec9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50ec9-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="50ec9-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="50ec9-116">Indica se eliminare gli abbonamenti al prodotto.</span><span class="sxs-lookup"><span data-stu-id="50ec9-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="50ec9-117">Se non si imposta questo parametro e non esiste una sottoscrizione, viene generata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="50ec9-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="50ec9-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50ec9-118">-PassThru</span></span>
<span data-ttu-id="50ec9-119">Indica che questo cmdlet restituisce un valore di $True, se ha esito positivo o un valore di $False, se non riesce.</span><span class="sxs-lookup"><span data-stu-id="50ec9-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="50ec9-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="50ec9-120">-ProductId</span></span>
<span data-ttu-id="50ec9-121">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="50ec9-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="50ec9-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="50ec9-122">-Confirm</span></span>
<span data-ttu-id="50ec9-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50ec9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50ec9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50ec9-124">-WhatIf</span></span>
<span data-ttu-id="50ec9-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50ec9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50ec9-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50ec9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50ec9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50ec9-127">CommonParameters</span></span>
<span data-ttu-id="50ec9-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50ec9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50ec9-129">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="50ec9-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50ec9-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50ec9-130">INPUTS</span></span>

### <span data-ttu-id="50ec9-131">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="50ec9-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="50ec9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="50ec9-132">System.String</span></span>

### <span data-ttu-id="50ec9-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="50ec9-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="50ec9-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50ec9-134">OUTPUTS</span></span>

### <span data-ttu-id="50ec9-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50ec9-135">System.Boolean</span></span>

## <span data-ttu-id="50ec9-136">Note</span><span class="sxs-lookup"><span data-stu-id="50ec9-136">NOTES</span></span>

## <span data-ttu-id="50ec9-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50ec9-137">RELATED LINKS</span></span>

[<span data-ttu-id="50ec9-138">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="50ec9-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="50ec9-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="50ec9-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="50ec9-140">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="50ec9-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


