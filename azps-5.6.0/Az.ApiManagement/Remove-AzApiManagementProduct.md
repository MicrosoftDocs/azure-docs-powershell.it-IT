---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 9ad08f867bf78dc4a6bc2df5c4dd3086c3cea33c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979022"
---
# <span data-ttu-id="97881-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="97881-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="97881-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97881-102">SYNOPSIS</span></span>
<span data-ttu-id="97881-103">Rimuove un prodotto di gestione delle API esistente.</span><span class="sxs-lookup"><span data-stu-id="97881-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="97881-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97881-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97881-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="97881-105">DESCRIPTION</span></span>
<span data-ttu-id="97881-106">Il cmdlet **Remove-AzApiManagementProduct** rimuove un prodotto gestione API esistente.</span><span class="sxs-lookup"><span data-stu-id="97881-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="97881-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97881-107">EXAMPLES</span></span>

### <span data-ttu-id="97881-108">Esempio 1: Rimuovere un prodotto esistente e tutti gli abbonamenti</span><span class="sxs-lookup"><span data-stu-id="97881-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="97881-109">Questo comando rimuove un prodotto esistente e tutte le sottoscrizioni.</span><span class="sxs-lookup"><span data-stu-id="97881-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="97881-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97881-110">PARAMETERS</span></span>

### <span data-ttu-id="97881-111">-Context</span><span class="sxs-lookup"><span data-stu-id="97881-111">-Context</span></span>
<span data-ttu-id="97881-112">Specifica un'istanza **dell'oggetto PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="97881-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="97881-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97881-113">-DefaultProfile</span></span>
<span data-ttu-id="97881-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97881-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97881-115">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="97881-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="97881-116">Indica se eliminare le sottoscrizioni per il prodotto.</span><span class="sxs-lookup"><span data-stu-id="97881-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="97881-117">Se non si imposta questo parametro e le sottoscrizioni esistono, viene generata un'eccezione.</span><span class="sxs-lookup"><span data-stu-id="97881-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="97881-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97881-118">-PassThru</span></span>
<span data-ttu-id="97881-119">Indica che questo cmdlet restituisce il valore $True, se ha esito positivo, oppure un valore $False, se ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="97881-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="97881-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="97881-120">-ProductId</span></span>
<span data-ttu-id="97881-121">Specifica l'identificatore del prodotto esistente.</span><span class="sxs-lookup"><span data-stu-id="97881-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="97881-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="97881-122">-Confirm</span></span>
<span data-ttu-id="97881-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97881-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97881-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97881-124">-WhatIf</span></span>
<span data-ttu-id="97881-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97881-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97881-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97881-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97881-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97881-127">CommonParameters</span></span>
<span data-ttu-id="97881-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97881-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97881-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="97881-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97881-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="97881-130">INPUTS</span></span>

### <span data-ttu-id="97881-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="97881-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="97881-132">System.String</span><span class="sxs-lookup"><span data-stu-id="97881-132">System.String</span></span>

### <span data-ttu-id="97881-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="97881-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="97881-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97881-134">OUTPUTS</span></span>

### <span data-ttu-id="97881-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="97881-135">System.Boolean</span></span>

## <span data-ttu-id="97881-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="97881-136">NOTES</span></span>

## <span data-ttu-id="97881-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97881-137">RELATED LINKS</span></span>

[<span data-ttu-id="97881-138">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="97881-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="97881-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="97881-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="97881-140">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="97881-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


