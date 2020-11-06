---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5981D3D8-E2E7-4905-8CD0-8BDC35BB39AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
ms.openlocfilehash: 7d8b2e02e5683f58eee06de1993f6ea0d4ecfac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507968"
---
# <span data-ttu-id="fb5a1-101">New-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="fb5a1-101">New-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="fb5a1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fb5a1-102">SYNOPSIS</span></span>
<span data-ttu-id="fb5a1-103">Crea una sessione di gestione del server.</span><span class="sxs-lookup"><span data-stu-id="fb5a1-103">Creates a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb5a1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb5a1-104">SYNTAX</span></span>

### <span data-ttu-id="fb5a1-105">ByName</span><span class="sxs-lookup"><span data-stu-id="fb5a1-105">ByName</span></span>
```
New-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName <String>]
 [-Credential <PSCredential>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb5a1-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="fb5a1-106">ByNode</span></span>
```
New-AzureRmServerManagementSession [-Node] <Node> [-SessionName <String>] [-Credential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb5a1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fb5a1-107">DESCRIPTION</span></span>
<span data-ttu-id="fb5a1-108">Il cmdlet **New-AzureRmServerManagementSession** crea una sessione di gestione di Azure server.</span><span class="sxs-lookup"><span data-stu-id="fb5a1-108">The **New-AzureRmServerManagementSession** cmdlet creates an Azure Server Management session.</span></span>

## <span data-ttu-id="fb5a1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb5a1-109">EXAMPLES</span></span>

## <span data-ttu-id="fb5a1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fb5a1-110">PARAMETERS</span></span>

### <span data-ttu-id="fb5a1-111">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="fb5a1-111">-Credential</span></span>
<span data-ttu-id="fb5a1-112">Specifica un oggetto **PSCredential** per la connessione alla sessione di gestione del server.</span><span class="sxs-lookup"><span data-stu-id="fb5a1-112">Specifies a **PSCredential** object for the connection to the Server Management Session.</span></span>
<span data-ttu-id="fb5a1-113">Per ottenere un oggetto Credential, usa il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="fb5a1-113">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="fb5a1-114">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="fb5a1-114">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb5a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb5a1-115">-DefaultProfile</span></span>
<span data-ttu-id="fb5a1-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fb5a1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb5a1-117">-Node</span><span class="sxs-lookup"><span data-stu-id="fb5a1-117">-Node</span></span>
<span data-ttu-id="fb5a1-118">Specifica il nodo per cui questo cmdlet crea la sessione.</span><span class="sxs-lookup"><span data-stu-id="fb5a1-118">Specifies the node for which this cmdlet creates the session on.</span></span>

<span data-ttu-id="fb5a1-119">Questo parametro può essere usato al posto dei parametri *ResourceGroupName* e *NodeName* .</span><span class="sxs-lookup"><span data-stu-id="fb5a1-119">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

```yaml
Type: Node
Parameter Sets: ByNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb5a1-120">-NodeName</span><span class="sxs-lookup"><span data-stu-id="fb5a1-120">-NodeName</span></span>
<span data-ttu-id="fb5a1-121">Specifica il nome del nodo per cui questo cmdlet crea una sessione.</span><span class="sxs-lookup"><span data-stu-id="fb5a1-121">Specifies the name of the node for which this cmdlet creates a session.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb5a1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb5a1-122">-ResourceGroupName</span></span>
<span data-ttu-id="fb5a1-123">Specifica il gruppo di risorse del nodo per cui questo cmdlet crea una sessione.</span><span class="sxs-lookup"><span data-stu-id="fb5a1-123">Specifies the resource group of the node that this cmdlet creates a session for.</span></span>

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

### <span data-ttu-id="fb5a1-124">-Sessionname</span><span class="sxs-lookup"><span data-stu-id="fb5a1-124">-SessionName</span></span>
<span data-ttu-id="fb5a1-125">Specifica il nome da usare per la sessione.</span><span class="sxs-lookup"><span data-stu-id="fb5a1-125">Specifies the name to use for the session.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb5a1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb5a1-126">CommonParameters</span></span>
<span data-ttu-id="fb5a1-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb5a1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb5a1-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb5a1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb5a1-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fb5a1-129">INPUTS</span></span>

### <span data-ttu-id="fb5a1-130">Nodo</span><span class="sxs-lookup"><span data-stu-id="fb5a1-130">Node</span></span>
<span data-ttu-id="fb5a1-131">Il parametro "node" accetta il valore di tipo "node" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="fb5a1-131">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="fb5a1-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb5a1-132">OUTPUTS</span></span>

### <span data-ttu-id="fb5a1-133">Microsoft. Azure. Commands. ServerManagement. Model. Session</span><span class="sxs-lookup"><span data-stu-id="fb5a1-133">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="fb5a1-134">Note</span><span class="sxs-lookup"><span data-stu-id="fb5a1-134">NOTES</span></span>

## <span data-ttu-id="fb5a1-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb5a1-135">RELATED LINKS</span></span>

