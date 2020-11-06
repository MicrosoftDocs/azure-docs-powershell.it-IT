---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementProductFromGroup.md
ms.openlocfilehash: 2eba88e94cfed3c253a5b5febc20a7585ab096d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508436"
---
# <span data-ttu-id="40ba8-101">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="40ba8-101">Remove-AzureRmApiManagementProductFromGroup</span></span>

## <span data-ttu-id="40ba8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="40ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="40ba8-103">Rimuove un prodotto da un gruppo.</span><span class="sxs-lookup"><span data-stu-id="40ba8-103">Removes a product from a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40ba8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="40ba8-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String>
 -ProductId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40ba8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40ba8-105">DESCRIPTION</span></span>
<span data-ttu-id="40ba8-106">Il cmdlet **Remove-AzureRmApiManagementProductFromGroup** rimuove un prodotto da un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="40ba8-106">The **Remove-AzureRmApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="40ba8-107">In altre parole, questo cmdlet rimuove l'assegnazione del gruppo da un prodotto.</span><span class="sxs-lookup"><span data-stu-id="40ba8-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="40ba8-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="40ba8-108">EXAMPLES</span></span>

### <span data-ttu-id="40ba8-109">Esempio 1: rimuovere un prodotto da un gruppo</span><span class="sxs-lookup"><span data-stu-id="40ba8-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="40ba8-110">Questo comando rimuove un prodotto da un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="40ba8-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="40ba8-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="40ba8-111">PARAMETERS</span></span>

### <span data-ttu-id="40ba8-112">-Contesto</span><span class="sxs-lookup"><span data-stu-id="40ba8-112">-Context</span></span>
<span data-ttu-id="40ba8-113">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="40ba8-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="40ba8-114">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="40ba8-114">This parameter is required.</span></span>

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

### <span data-ttu-id="40ba8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40ba8-115">-DefaultProfile</span></span>
<span data-ttu-id="40ba8-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="40ba8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="40ba8-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="40ba8-117">-GroupId</span></span>
<span data-ttu-id="40ba8-118">Specifica l'ID del gruppo.</span><span class="sxs-lookup"><span data-stu-id="40ba8-118">Specifies the group ID.</span></span>
<span data-ttu-id="40ba8-119">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="40ba8-119">This parameter is required.</span></span>

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

### <span data-ttu-id="40ba8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40ba8-120">-PassThru</span></span>
<span data-ttu-id="40ba8-121">Indica che questo cmdlet restituisce un valore di $True, se ha esito positivo o $False, in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="40ba8-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="40ba8-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="40ba8-122">-ProductId</span></span>
<span data-ttu-id="40ba8-123">Specifica l'ID prodotto.</span><span class="sxs-lookup"><span data-stu-id="40ba8-123">Specifies the product ID.</span></span>
<span data-ttu-id="40ba8-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="40ba8-124">This parameter is required.</span></span>

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

### <span data-ttu-id="40ba8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40ba8-125">CommonParameters</span></span>
<span data-ttu-id="40ba8-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40ba8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40ba8-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40ba8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40ba8-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="40ba8-128">INPUTS</span></span>

### <span data-ttu-id="40ba8-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="40ba8-129">None</span></span>
<span data-ttu-id="40ba8-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="40ba8-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="40ba8-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="40ba8-131">OUTPUTS</span></span>

### <span data-ttu-id="40ba8-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="40ba8-132">System.Boolean</span></span>

## <span data-ttu-id="40ba8-133">Note</span><span class="sxs-lookup"><span data-stu-id="40ba8-133">NOTES</span></span>

## <span data-ttu-id="40ba8-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="40ba8-134">RELATED LINKS</span></span>

[<span data-ttu-id="40ba8-135">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="40ba8-135">Add-AzureRmApiManagementProductToGroup</span></span>](./Add-AzureRmApiManagementProductToGroup.md)


