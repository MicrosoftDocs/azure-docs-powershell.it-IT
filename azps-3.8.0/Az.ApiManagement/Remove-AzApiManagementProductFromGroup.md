---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
ms.openlocfilehash: a2afd2d5296912606363eddab49e0e3d6b371538
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020100"
---
# <span data-ttu-id="39067-101">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="39067-101">Remove-AzApiManagementProductFromGroup</span></span>

## <span data-ttu-id="39067-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="39067-102">SYNOPSIS</span></span>
<span data-ttu-id="39067-103">Rimuove un prodotto da un gruppo.</span><span class="sxs-lookup"><span data-stu-id="39067-103">Removes a product from a group.</span></span>

## <span data-ttu-id="39067-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39067-104">SYNTAX</span></span>

```
Remove-AzApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39067-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="39067-105">DESCRIPTION</span></span>
<span data-ttu-id="39067-106">Il cmdlet **Remove-AzApiManagementProductFromGroup** rimuove un prodotto da un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="39067-106">The **Remove-AzApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="39067-107">In altre parole, questo cmdlet rimuove l'assegnazione del gruppo da un prodotto.</span><span class="sxs-lookup"><span data-stu-id="39067-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="39067-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39067-108">EXAMPLES</span></span>

### <span data-ttu-id="39067-109">Esempio 1: rimuovere un prodotto da un gruppo</span><span class="sxs-lookup"><span data-stu-id="39067-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="39067-110">Questo comando rimuove un prodotto da un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="39067-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="39067-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="39067-111">PARAMETERS</span></span>

### <span data-ttu-id="39067-112">-Contesto</span><span class="sxs-lookup"><span data-stu-id="39067-112">-Context</span></span>
<span data-ttu-id="39067-113">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="39067-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="39067-114">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="39067-114">This parameter is required.</span></span>

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

### <span data-ttu-id="39067-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39067-115">-DefaultProfile</span></span>
<span data-ttu-id="39067-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39067-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39067-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="39067-117">-GroupId</span></span>
<span data-ttu-id="39067-118">Specifica l'ID del gruppo.</span><span class="sxs-lookup"><span data-stu-id="39067-118">Specifies the group ID.</span></span>
<span data-ttu-id="39067-119">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="39067-119">This parameter is required.</span></span>

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

### <span data-ttu-id="39067-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39067-120">-PassThru</span></span>
<span data-ttu-id="39067-121">Indica che questo cmdlet restituisce un valore di $True, se ha esito positivo o $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="39067-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="39067-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="39067-122">-ProductId</span></span>
<span data-ttu-id="39067-123">Specifica l'ID prodotto.</span><span class="sxs-lookup"><span data-stu-id="39067-123">Specifies the product ID.</span></span>
<span data-ttu-id="39067-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="39067-124">This parameter is required.</span></span>

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

### <span data-ttu-id="39067-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39067-125">CommonParameters</span></span>
<span data-ttu-id="39067-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39067-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39067-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="39067-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39067-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="39067-128">INPUTS</span></span>

### <span data-ttu-id="39067-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="39067-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="39067-130">System. String</span><span class="sxs-lookup"><span data-stu-id="39067-130">System.String</span></span>

### <span data-ttu-id="39067-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="39067-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="39067-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39067-132">OUTPUTS</span></span>

### <span data-ttu-id="39067-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="39067-133">System.Boolean</span></span>

## <span data-ttu-id="39067-134">Note</span><span class="sxs-lookup"><span data-stu-id="39067-134">NOTES</span></span>

## <span data-ttu-id="39067-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39067-135">RELATED LINKS</span></span>

[<span data-ttu-id="39067-136">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="39067-136">Add-AzApiManagementProductToGroup</span></span>](./Add-AzApiManagementProductToGroup.md)


