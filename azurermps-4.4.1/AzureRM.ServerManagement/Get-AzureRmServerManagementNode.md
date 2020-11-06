---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 4EE30890-B09B-4811-88AD-4BF4FD47E431
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementNode.md
ms.openlocfilehash: ab49458426b7035a20e63ca62d86124d79291b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516052"
---
# <span data-ttu-id="53e79-101">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="53e79-101">Get-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="53e79-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53e79-102">SYNOPSIS</span></span>
<span data-ttu-id="53e79-103">Ottiene uno o più nodi di gestione del server.</span><span class="sxs-lookup"><span data-stu-id="53e79-103">Gets one or more Server Management nodes.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53e79-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53e79-104">SYNTAX</span></span>

### <span data-ttu-id="53e79-105">ByNodeName</span><span class="sxs-lookup"><span data-stu-id="53e79-105">ByNodeName</span></span>
```
Get-AzureRmServerManagementNode [[-ResourceGroupName] <String>] [[-NodeName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53e79-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="53e79-106">ByNode</span></span>
```
Get-AzureRmServerManagementNode [-Node] <Node> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53e79-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53e79-107">DESCRIPTION</span></span>
<span data-ttu-id="53e79-108">Il cmdlet **Get-AzureRmServerManagementNode** ottiene uno o più nodi di gestione di Azure server.</span><span class="sxs-lookup"><span data-stu-id="53e79-108">The **Get-AzureRmServerManagementNode** cmdlet gets one or more Azure Server Management nodes.</span></span>

## <span data-ttu-id="53e79-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53e79-109">EXAMPLES</span></span>

## <span data-ttu-id="53e79-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53e79-110">PARAMETERS</span></span>

### <span data-ttu-id="53e79-111">-Node</span><span class="sxs-lookup"><span data-stu-id="53e79-111">-Node</span></span>
<span data-ttu-id="53e79-112">Specifica un nodo esistente da cui ottenere i parametri *ResourceGroupName* e *NodeName* .</span><span class="sxs-lookup"><span data-stu-id="53e79-112">Specifies an existing node from which to get the *ResourceGroupName* and the *NodeName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Node
Parameter Sets: ByNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53e79-113">-NodeName</span><span class="sxs-lookup"><span data-stu-id="53e79-113">-NodeName</span></span>
<span data-ttu-id="53e79-114">Specifica il nome del nodo per cui viene ottenuto questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53e79-114">Specifies the name of the node for which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53e79-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53e79-115">-ResourceGroupName</span></span>
<span data-ttu-id="53e79-116">Specifica il nome del gruppo di risorse a cui appartengono i nodi.</span><span class="sxs-lookup"><span data-stu-id="53e79-116">Specifies the name of the resource group in which the nodes belong to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53e79-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53e79-117">-DefaultProfile</span></span>
<span data-ttu-id="53e79-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="53e79-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53e79-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53e79-119">CommonParameters</span></span>
<span data-ttu-id="53e79-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53e79-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53e79-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53e79-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53e79-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53e79-122">INPUTS</span></span>

### <span data-ttu-id="53e79-123">Nodo</span><span class="sxs-lookup"><span data-stu-id="53e79-123">Node</span></span>
<span data-ttu-id="53e79-124">Il parametro "node" accetta il valore di tipo "node" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="53e79-124">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="53e79-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53e79-125">OUTPUTS</span></span>

### <span data-ttu-id="53e79-126">Microsoft. Azure. Commands. ServerManagement. Model. Node</span><span class="sxs-lookup"><span data-stu-id="53e79-126">Microsoft.Azure.Commands.ServerManagement.Model.Node</span></span>

## <span data-ttu-id="53e79-127">Note</span><span class="sxs-lookup"><span data-stu-id="53e79-127">NOTES</span></span>

## <span data-ttu-id="53e79-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53e79-128">RELATED LINKS</span></span>

[<span data-ttu-id="53e79-129">New-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="53e79-129">New-AzureRmServerManagementNode</span></span>](./New-AzureRmServerManagementNode.md)

[<span data-ttu-id="53e79-130">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="53e79-130">Remove-AzureRmServerManagementNode</span></span>](./Remove-AzureRmServerManagementNode.md)


