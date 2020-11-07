---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 41F8F851-6F9F-4DA4-8CE6-D8C9B7CF68D7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/remove-azurermservermanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementGateway.md
ms.openlocfilehash: 53bf195bf801b4746f0ea958949f1683c8ca3d0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687006"
---
# <span data-ttu-id="22519-101">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="22519-101">Remove-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="22519-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22519-102">SYNOPSIS</span></span>
<span data-ttu-id="22519-103">Rimuove un gateway di gestione server.</span><span class="sxs-lookup"><span data-stu-id="22519-103">Removes a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22519-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22519-104">SYNTAX</span></span>

### <span data-ttu-id="22519-105">ByName</span><span class="sxs-lookup"><span data-stu-id="22519-105">ByName</span></span>
```
Remove-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22519-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="22519-106">ByObject</span></span>
```
Remove-AzureRmServerManagementGateway [-Gateway] <Gateway> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22519-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22519-107">DESCRIPTION</span></span>
<span data-ttu-id="22519-108">Il cmdlet **Remove-AzureRmServerManagementGateway** rimuove un gateway di gestione di Azure server.</span><span class="sxs-lookup"><span data-stu-id="22519-108">The **Remove-AzureRmServerManagementGateway** cmdlet removes an Azure Server Management gateway.</span></span>

## <span data-ttu-id="22519-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22519-109">EXAMPLES</span></span>

## <span data-ttu-id="22519-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22519-110">PARAMETERS</span></span>

### <span data-ttu-id="22519-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22519-111">-DefaultProfile</span></span>
<span data-ttu-id="22519-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="22519-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22519-113">-Gateway</span><span class="sxs-lookup"><span data-stu-id="22519-113">-Gateway</span></span>
<span data-ttu-id="22519-114">Specifica il gateway rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22519-114">Specifies the gateway that this cmdlet removes.</span></span>

<span data-ttu-id="22519-115">Questo parametro può essere usato al posto dei parametri *ResourceGroupName* e *GatewayName* .</span><span class="sxs-lookup"><span data-stu-id="22519-115">This parameter may be used instead of the *ResourceGroupName* and the *GatewayName* parameters.</span></span>

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="22519-116">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="22519-116">-GatewayName</span></span>
<span data-ttu-id="22519-117">Specifica il nome del gateway rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22519-117">Specifies the name of the gateway that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22519-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22519-118">-ResourceGroupName</span></span>
<span data-ttu-id="22519-119">Specifica il nome del gruppo di risorse a cui appartiene il gateway.</span><span class="sxs-lookup"><span data-stu-id="22519-119">Specifies the name of the resource group in that the gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22519-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22519-120">CommonParameters</span></span>
<span data-ttu-id="22519-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22519-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22519-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22519-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22519-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22519-123">INPUTS</span></span>

### <span data-ttu-id="22519-124">Gateway</span><span class="sxs-lookup"><span data-stu-id="22519-124">Gateway</span></span>
<span data-ttu-id="22519-125">Il parametro "gateway" accetta il valore di tipo "gateway" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="22519-125">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="22519-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22519-126">OUTPUTS</span></span>

## <span data-ttu-id="22519-127">Note</span><span class="sxs-lookup"><span data-stu-id="22519-127">NOTES</span></span>
* <span data-ttu-id="22519-128">Tutti i nodi del gateway devono essere rimossi prima di usare questo cmdlet; in caso contrario, il cmdlet avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="22519-128">All the nodes in the Gateway must be removed before using this cmdlet; otherwise this cmdlet will fail.</span></span>

## <span data-ttu-id="22519-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22519-129">RELATED LINKS</span></span>

[<span data-ttu-id="22519-130">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="22519-130">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="22519-131">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="22519-131">New-AzureRmServerManagementGateway</span></span>](./New-AzureRmServerManagementGateway.md)


