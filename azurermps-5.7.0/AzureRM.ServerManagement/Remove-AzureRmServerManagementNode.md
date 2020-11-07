---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: B66C7A03-862A-497D-977B-1C43089DE24B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/remove-azurermservermanagementnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementNode.md
ms.openlocfilehash: 78fa17dee687547b617ff02dd11ecbf662e48040
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685602"
---
# <span data-ttu-id="ba7eb-101">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="ba7eb-101">Remove-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="ba7eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ba7eb-102">SYNOPSIS</span></span>
<span data-ttu-id="ba7eb-103">Rimuove un nodo di gestione del server.</span><span class="sxs-lookup"><span data-stu-id="ba7eb-103">Removes a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba7eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ba7eb-104">SYNTAX</span></span>

### <span data-ttu-id="ba7eb-105">ByName</span><span class="sxs-lookup"><span data-stu-id="ba7eb-105">ByName</span></span>
```
Remove-AzureRmServerManagementNode [-ResourceGroupName] <String> [-NodeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba7eb-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="ba7eb-106">ByObject</span></span>
```
Remove-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba7eb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba7eb-107">DESCRIPTION</span></span>
<span data-ttu-id="ba7eb-108">Il cmdlet **Remove-AzureRmServerManagementNode** rimuove un nodo di gestione di Azure server.</span><span class="sxs-lookup"><span data-stu-id="ba7eb-108">The **Remove-AzureRmServerManagementNode** cmdlet removes an Azure Server Management node.</span></span>

## <span data-ttu-id="ba7eb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ba7eb-109">EXAMPLES</span></span>

## <span data-ttu-id="ba7eb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ba7eb-110">PARAMETERS</span></span>

### <span data-ttu-id="ba7eb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba7eb-111">-DefaultProfile</span></span>
<span data-ttu-id="ba7eb-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ba7eb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba7eb-113">-Node</span><span class="sxs-lookup"><span data-stu-id="ba7eb-113">-Node</span></span>
<span data-ttu-id="ba7eb-114">Specifica il nodo di cui viene rimosso questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba7eb-114">Specifies the node for which this cmdlet removes.</span></span>

<span data-ttu-id="ba7eb-115">Questo parametro può essere usato al posto dei parametri *ResourceGroupName* e *NodeName* .</span><span class="sxs-lookup"><span data-stu-id="ba7eb-115">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

```yaml
Type: Node
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba7eb-116">-NodeName</span><span class="sxs-lookup"><span data-stu-id="ba7eb-116">-NodeName</span></span>
<span data-ttu-id="ba7eb-117">Specifica il nome del nodo di cui viene rimosso il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba7eb-117">Specifies the name of the node for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="ba7eb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba7eb-118">-ResourceGroupName</span></span>
<span data-ttu-id="ba7eb-119">Specifica il nome del gruppo di risorse a cui appartiene il nodo.</span><span class="sxs-lookup"><span data-stu-id="ba7eb-119">Specifies the name of the resource group that the node belongs to.</span></span>

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

### <span data-ttu-id="ba7eb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba7eb-120">CommonParameters</span></span>
<span data-ttu-id="ba7eb-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba7eb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba7eb-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba7eb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba7eb-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ba7eb-123">INPUTS</span></span>

### <span data-ttu-id="ba7eb-124">Nodo</span><span class="sxs-lookup"><span data-stu-id="ba7eb-124">Node</span></span>
<span data-ttu-id="ba7eb-125">Il parametro "node" accetta il valore di tipo "node" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ba7eb-125">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="ba7eb-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ba7eb-126">OUTPUTS</span></span>

## <span data-ttu-id="ba7eb-127">Note</span><span class="sxs-lookup"><span data-stu-id="ba7eb-127">NOTES</span></span>

## <span data-ttu-id="ba7eb-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ba7eb-128">RELATED LINKS</span></span>

[<span data-ttu-id="ba7eb-129">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="ba7eb-129">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="ba7eb-130">New-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="ba7eb-130">New-AzureRmServerManagementNode</span></span>](./New-AzureRmServerManagementNode.md)


