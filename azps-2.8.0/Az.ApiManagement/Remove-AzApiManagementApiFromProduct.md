---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: 497e830ff5ee51a9b18480a4d3f31f7c51949723
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675963"
---
# <span data-ttu-id="00078-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="00078-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="00078-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="00078-102">SYNOPSIS</span></span>
<span data-ttu-id="00078-103">Rimuove un'API da un prodotto.</span><span class="sxs-lookup"><span data-stu-id="00078-103">Removes an API from a product.</span></span>

## <span data-ttu-id="00078-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00078-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00078-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00078-105">DESCRIPTION</span></span>
<span data-ttu-id="00078-106">Il cmdlet **Remove-AzApiManagementApiFromProduct** rimuove un'API di gestione delle API di Azure da un prodotto.</span><span class="sxs-lookup"><span data-stu-id="00078-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="00078-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00078-107">EXAMPLES</span></span>

### <span data-ttu-id="00078-108">Esempio 1: rimuovere un'API da un prodotto</span><span class="sxs-lookup"><span data-stu-id="00078-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="00078-109">Questo comando rimuove l'API specificata da un prodotto.</span><span class="sxs-lookup"><span data-stu-id="00078-109">This command removes the specified API from a product.</span></span>

## <span data-ttu-id="00078-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="00078-110">PARAMETERS</span></span>

### <span data-ttu-id="00078-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="00078-111">-ApiId</span></span>
<span data-ttu-id="00078-112">Specifica l'ID dell'API da rimuovere dal prodotto.</span><span class="sxs-lookup"><span data-stu-id="00078-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="00078-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="00078-113">-Context</span></span>
<span data-ttu-id="00078-114">Specifica un **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="00078-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="00078-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00078-115">-DefaultProfile</span></span>
<span data-ttu-id="00078-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="00078-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00078-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00078-117">-PassThru</span></span>
<span data-ttu-id="00078-118">Indica che questo cmdlet restituisce un valore di $True se riesce o $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="00078-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="00078-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="00078-119">-ProductId</span></span>
<span data-ttu-id="00078-120">Specifica l'ID del prodotto da cui rimuovere l'API.</span><span class="sxs-lookup"><span data-stu-id="00078-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="00078-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00078-121">CommonParameters</span></span>
<span data-ttu-id="00078-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00078-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00078-123">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00078-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00078-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="00078-124">INPUTS</span></span>

### <span data-ttu-id="00078-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="00078-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="00078-126">System. String</span><span class="sxs-lookup"><span data-stu-id="00078-126">System.String</span></span>

### <span data-ttu-id="00078-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="00078-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="00078-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00078-128">OUTPUTS</span></span>

### <span data-ttu-id="00078-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="00078-129">System.Boolean</span></span>

## <span data-ttu-id="00078-130">Note</span><span class="sxs-lookup"><span data-stu-id="00078-130">NOTES</span></span>

## <span data-ttu-id="00078-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00078-131">RELATED LINKS</span></span>

[<span data-ttu-id="00078-132">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="00078-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


