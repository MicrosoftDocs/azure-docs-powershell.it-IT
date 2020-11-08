---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: fd9e4cec821b08c9ac2bbd5cd2ac43e5e5b114ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191708"
---
# <span data-ttu-id="87b1c-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="87b1c-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="87b1c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="87b1c-102">SYNOPSIS</span></span>
<span data-ttu-id="87b1c-103">Rimuove un'API da un prodotto.</span><span class="sxs-lookup"><span data-stu-id="87b1c-103">Removes an API from a product.</span></span>

## <span data-ttu-id="87b1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="87b1c-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87b1c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="87b1c-105">DESCRIPTION</span></span>
<span data-ttu-id="87b1c-106">Il cmdlet **Remove-AzApiManagementApiFromProduct** rimuove un'API di gestione delle API di Azure da un prodotto.</span><span class="sxs-lookup"><span data-stu-id="87b1c-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="87b1c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="87b1c-107">EXAMPLES</span></span>

### <span data-ttu-id="87b1c-108">Esempio 1: rimuovere un'API da un prodotto</span><span class="sxs-lookup"><span data-stu-id="87b1c-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="87b1c-109">Questo comando rimuove l'API specificata da un prodotto.</span><span class="sxs-lookup"><span data-stu-id="87b1c-109">This command removes the specified API from a product.</span></span>

## <span data-ttu-id="87b1c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="87b1c-110">PARAMETERS</span></span>

### <span data-ttu-id="87b1c-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="87b1c-111">-ApiId</span></span>
<span data-ttu-id="87b1c-112">Specifica l'ID dell'API da rimuovere dal prodotto.</span><span class="sxs-lookup"><span data-stu-id="87b1c-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="87b1c-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="87b1c-113">-Context</span></span>
<span data-ttu-id="87b1c-114">Specifica un **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="87b1c-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="87b1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87b1c-115">-DefaultProfile</span></span>
<span data-ttu-id="87b1c-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="87b1c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87b1c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="87b1c-117">-PassThru</span></span>
<span data-ttu-id="87b1c-118">Indica che questo cmdlet restituisce un valore di $True se riesce o $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="87b1c-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="87b1c-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="87b1c-119">-ProductId</span></span>
<span data-ttu-id="87b1c-120">Specifica l'ID del prodotto da cui rimuovere l'API.</span><span class="sxs-lookup"><span data-stu-id="87b1c-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="87b1c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87b1c-121">CommonParameters</span></span>
<span data-ttu-id="87b1c-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87b1c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87b1c-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87b1c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87b1c-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="87b1c-124">INPUTS</span></span>

### <span data-ttu-id="87b1c-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="87b1c-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="87b1c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="87b1c-126">System.String</span></span>

### <span data-ttu-id="87b1c-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="87b1c-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="87b1c-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="87b1c-128">OUTPUTS</span></span>

### <span data-ttu-id="87b1c-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="87b1c-129">System.Boolean</span></span>

## <span data-ttu-id="87b1c-130">Note</span><span class="sxs-lookup"><span data-stu-id="87b1c-130">NOTES</span></span>

## <span data-ttu-id="87b1c-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="87b1c-131">RELATED LINKS</span></span>

[<span data-ttu-id="87b1c-132">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="87b1c-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)

