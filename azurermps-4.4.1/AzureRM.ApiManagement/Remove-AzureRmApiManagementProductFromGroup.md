---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
ms.openlocfilehash: a6ef7e141863b6dfd98185df0f8e3cfbd85ae40b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508807"
---
# <span data-ttu-id="f761a-101">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="f761a-101">Remove-AzureRmApiManagementProductFromGroup</span></span>

## <span data-ttu-id="f761a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f761a-102">SYNOPSIS</span></span>
<span data-ttu-id="f761a-103">Rimuove un prodotto da un gruppo.</span><span class="sxs-lookup"><span data-stu-id="f761a-103">Removes a product from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f761a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f761a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String>
 -ProductId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f761a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f761a-105">DESCRIPTION</span></span>
<span data-ttu-id="f761a-106">Il cmdlet **Remove-AzureRmApiManagementProductFromGroup** rimuove un prodotto da un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="f761a-106">The **Remove-AzureRmApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="f761a-107">In altre parole, questo cmdlet rimuove l'assegnazione del gruppo da un prodotto.</span><span class="sxs-lookup"><span data-stu-id="f761a-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="f761a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f761a-108">EXAMPLES</span></span>

### <span data-ttu-id="f761a-109">Esempio 1: rimuovere un prodotto da un gruppo</span><span class="sxs-lookup"><span data-stu-id="f761a-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>Remove-AzureRmApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="f761a-110">Questo comando rimuove un prodotto da un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="f761a-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="f761a-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f761a-111">PARAMETERS</span></span>

### <span data-ttu-id="f761a-112">-Contesto</span><span class="sxs-lookup"><span data-stu-id="f761a-112">-Context</span></span>
<span data-ttu-id="f761a-113">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f761a-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f761a-114">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f761a-114">This parameter is required.</span></span>

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

### <span data-ttu-id="f761a-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="f761a-115">-GroupId</span></span>
<span data-ttu-id="f761a-116">Specifica l'ID del gruppo.</span><span class="sxs-lookup"><span data-stu-id="f761a-116">Specifies the group ID.</span></span>
<span data-ttu-id="f761a-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f761a-117">This parameter is required.</span></span>

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

### <span data-ttu-id="f761a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f761a-118">-PassThru</span></span>
<span data-ttu-id="f761a-119">Indica che questo cmdlet restituisce un valore di $True, se ha esito positivo o $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f761a-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="f761a-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="f761a-120">-ProductId</span></span>
<span data-ttu-id="f761a-121">Specifica l'ID prodotto.</span><span class="sxs-lookup"><span data-stu-id="f761a-121">Specifies the product ID.</span></span>
<span data-ttu-id="f761a-122">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f761a-122">This parameter is required.</span></span>

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

### <span data-ttu-id="f761a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f761a-123">-DefaultProfile</span></span>
<span data-ttu-id="f761a-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f761a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f761a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f761a-125">CommonParameters</span></span>
<span data-ttu-id="f761a-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f761a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f761a-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f761a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f761a-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f761a-128">INPUTS</span></span>

## <span data-ttu-id="f761a-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f761a-129">OUTPUTS</span></span>

### <span data-ttu-id="f761a-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f761a-130">System.Boolean</span></span>

## <span data-ttu-id="f761a-131">Note</span><span class="sxs-lookup"><span data-stu-id="f761a-131">NOTES</span></span>

## <span data-ttu-id="f761a-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f761a-132">RELATED LINKS</span></span>

[<span data-ttu-id="f761a-133">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="f761a-133">Add-AzureRmApiManagementProductToGroup</span></span>](./Add-AzureRmApiManagementProductToGroup.md)


