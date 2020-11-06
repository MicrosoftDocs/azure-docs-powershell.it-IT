---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementProductToGroup.md
ms.openlocfilehash: b4e1a029eca4e7eda48f44d85292639767eaf845
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519655"
---
# <span data-ttu-id="9aa68-101">Add-AzureRmApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="9aa68-101">Add-AzureRmApiManagementProductToGroup</span></span>

## <span data-ttu-id="9aa68-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9aa68-102">SYNOPSIS</span></span>
<span data-ttu-id="9aa68-103">Aggiunge un prodotto a un gruppo.</span><span class="sxs-lookup"><span data-stu-id="9aa68-103">Adds a product to a group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9aa68-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9aa68-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9aa68-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9aa68-105">DESCRIPTION</span></span>
<span data-ttu-id="9aa68-106">Il cmdlet **Add-AzureRmApiManagementProductToGroup** aggiunge un prodotto a un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="9aa68-106">The **Add-AzureRmApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="9aa68-107">In altre parole, questo cmdlet assegna un gruppo a un prodotto.</span><span class="sxs-lookup"><span data-stu-id="9aa68-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="9aa68-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9aa68-108">EXAMPLES</span></span>

### <span data-ttu-id="9aa68-109">Esempio 1: aggiungere un prodotto a un gruppo</span><span class="sxs-lookup"><span data-stu-id="9aa68-109">Example 1: Add a product to a group</span></span>
```
PS C:\>Add-AzureRmApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="9aa68-110">Questo comando aggiunge un prodotto a un gruppo esistente.</span><span class="sxs-lookup"><span data-stu-id="9aa68-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="9aa68-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9aa68-111">PARAMETERS</span></span>

### <span data-ttu-id="9aa68-112">-Contesto</span><span class="sxs-lookup"><span data-stu-id="9aa68-112">-Context</span></span>
<span data-ttu-id="9aa68-113">Specifica un oggetto **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="9aa68-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="9aa68-114">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9aa68-114">This parameter is required.</span></span>

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

### <span data-ttu-id="9aa68-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="9aa68-115">-GroupId</span></span>
<span data-ttu-id="9aa68-116">Specifica l'ID del gruppo.</span><span class="sxs-lookup"><span data-stu-id="9aa68-116">Specifies the group ID.</span></span>
<span data-ttu-id="9aa68-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9aa68-117">This parameter is required.</span></span>

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

### <span data-ttu-id="9aa68-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9aa68-118">-PassThru</span></span>
<span data-ttu-id="9aa68-119">PassThru</span><span class="sxs-lookup"><span data-stu-id="9aa68-119">passthru</span></span>

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

### <span data-ttu-id="9aa68-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="9aa68-120">-ProductId</span></span>
<span data-ttu-id="9aa68-121">Specifica l'ID prodotto.</span><span class="sxs-lookup"><span data-stu-id="9aa68-121">Specifies the product ID.</span></span>
<span data-ttu-id="9aa68-122">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9aa68-122">This parameter is required.</span></span>

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

### <span data-ttu-id="9aa68-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aa68-123">-DefaultProfile</span></span>
<span data-ttu-id="9aa68-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9aa68-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9aa68-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aa68-125">CommonParameters</span></span>
<span data-ttu-id="9aa68-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9aa68-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aa68-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9aa68-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aa68-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9aa68-128">INPUTS</span></span>

## <span data-ttu-id="9aa68-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9aa68-129">OUTPUTS</span></span>

### <span data-ttu-id="9aa68-130">Boolean</span><span class="sxs-lookup"><span data-stu-id="9aa68-130">Boolean</span></span>

## <span data-ttu-id="9aa68-131">Note</span><span class="sxs-lookup"><span data-stu-id="9aa68-131">NOTES</span></span>

## <span data-ttu-id="9aa68-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9aa68-132">RELATED LINKS</span></span>

[<span data-ttu-id="9aa68-133">Remove-AzureRmApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="9aa68-133">Remove-AzureRmApiManagementProductFromGroup</span></span>](./Remove-AzureRmApiManagementProductFromGroup.md)


