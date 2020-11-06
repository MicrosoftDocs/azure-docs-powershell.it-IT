---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 5981D3D8-E2E7-4905-8CD0-8BDC35BB39AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementSession.md
ms.openlocfilehash: 0ae3e221ee39a00381f009f45a9a2f508a552b6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512991"
---
# <span data-ttu-id="1eb30-101">New-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="1eb30-101">New-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="1eb30-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1eb30-102">SYNOPSIS</span></span>
<span data-ttu-id="1eb30-103">Crea una sessione di gestione del server.</span><span class="sxs-lookup"><span data-stu-id="1eb30-103">Creates a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1eb30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1eb30-104">SYNTAX</span></span>

### <span data-ttu-id="1eb30-105">ByName</span><span class="sxs-lookup"><span data-stu-id="1eb30-105">ByName</span></span>
```
New-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName <String>]
 [-Credential <PSCredential>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1eb30-106">ByNode</span><span class="sxs-lookup"><span data-stu-id="1eb30-106">ByNode</span></span>
```
New-AzureRmServerManagementSession [-Node] <Node> [-SessionName <String>] [-Credential <PSCredential>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1eb30-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1eb30-107">DESCRIPTION</span></span>
<span data-ttu-id="1eb30-108">Il cmdlet **New-AzureRmServerManagementSession** crea una sessione di gestione di Azure server.</span><span class="sxs-lookup"><span data-stu-id="1eb30-108">The **New-AzureRmServerManagementSession** cmdlet creates an Azure Server Management session.</span></span>

## <span data-ttu-id="1eb30-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1eb30-109">EXAMPLES</span></span>

## <span data-ttu-id="1eb30-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1eb30-110">PARAMETERS</span></span>

### <span data-ttu-id="1eb30-111">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="1eb30-111">-Credential</span></span>
<span data-ttu-id="1eb30-112">Specifica un oggetto **PSCredential** per la connessione alla sessione di gestione del server.</span><span class="sxs-lookup"><span data-stu-id="1eb30-112">Specifies a **PSCredential** object for the connection to the Server Management Session.</span></span>
<span data-ttu-id="1eb30-113">Per ottenere un oggetto Credential, usa il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="1eb30-113">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="1eb30-114">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="1eb30-114">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eb30-115">-Node</span><span class="sxs-lookup"><span data-stu-id="1eb30-115">-Node</span></span>
<span data-ttu-id="1eb30-116">Specifica il nodo per cui questo cmdlet crea la sessione.</span><span class="sxs-lookup"><span data-stu-id="1eb30-116">Specifies the node for which this cmdlet creates the session on.</span></span>

<span data-ttu-id="1eb30-117">Questo parametro può essere usato al posto dei parametri *ResourceGroupName* e *NodeName* .</span><span class="sxs-lookup"><span data-stu-id="1eb30-117">This parameter may be used instead of the *ResourceGroupName* and *NodeName* parameters.</span></span>

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

### <span data-ttu-id="1eb30-118">-NodeName</span><span class="sxs-lookup"><span data-stu-id="1eb30-118">-NodeName</span></span>
<span data-ttu-id="1eb30-119">Specifica il nome del nodo per cui questo cmdlet crea una sessione.</span><span class="sxs-lookup"><span data-stu-id="1eb30-119">Specifies the name of the node for which this cmdlet creates a session.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1eb30-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1eb30-120">-ResourceGroupName</span></span>
<span data-ttu-id="1eb30-121">Specifica il gruppo di risorse del nodo per cui questo cmdlet crea una sessione.</span><span class="sxs-lookup"><span data-stu-id="1eb30-121">Specifies the resource group of the node that this cmdlet creates a session for.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1eb30-122">-Sessionname</span><span class="sxs-lookup"><span data-stu-id="1eb30-122">-SessionName</span></span>
<span data-ttu-id="1eb30-123">Specifica il nome da usare per la sessione.</span><span class="sxs-lookup"><span data-stu-id="1eb30-123">Specifies the name to use for the session.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1eb30-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1eb30-124">-DefaultProfile</span></span>
<span data-ttu-id="1eb30-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1eb30-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1eb30-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1eb30-126">CommonParameters</span></span>
<span data-ttu-id="1eb30-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1eb30-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1eb30-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1eb30-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1eb30-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1eb30-129">INPUTS</span></span>

### <span data-ttu-id="1eb30-130">Nodo</span><span class="sxs-lookup"><span data-stu-id="1eb30-130">Node</span></span>
<span data-ttu-id="1eb30-131">Il parametro "node" accetta il valore di tipo "node" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="1eb30-131">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

## <span data-ttu-id="1eb30-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1eb30-132">OUTPUTS</span></span>

### <span data-ttu-id="1eb30-133">Microsoft. Azure. Commands. ServerManagement. Model. Session</span><span class="sxs-lookup"><span data-stu-id="1eb30-133">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="1eb30-134">Note</span><span class="sxs-lookup"><span data-stu-id="1eb30-134">NOTES</span></span>

## <span data-ttu-id="1eb30-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1eb30-135">RELATED LINKS</span></span>

