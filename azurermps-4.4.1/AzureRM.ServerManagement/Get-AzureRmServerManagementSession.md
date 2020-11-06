---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 8942D757-B204-49CE-BCDE-68C3722913B3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementSession.md
ms.openlocfilehash: e3388a06a2835fcd9865a9aa46d376b693152bc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516048"
---
# <span data-ttu-id="994eb-101">Get-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="994eb-101">Get-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="994eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="994eb-102">SYNOPSIS</span></span>
<span data-ttu-id="994eb-103">Ottiene una sessione di gestione del server.</span><span class="sxs-lookup"><span data-stu-id="994eb-103">Gets a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="994eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="994eb-104">SYNTAX</span></span>

### <span data-ttu-id="994eb-105">ByNodeName</span><span class="sxs-lookup"><span data-stu-id="994eb-105">ByNodeName</span></span>
```
Get-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="994eb-106">BySession</span><span class="sxs-lookup"><span data-stu-id="994eb-106">BySession</span></span>
```
Get-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="994eb-107">ByNode</span><span class="sxs-lookup"><span data-stu-id="994eb-107">ByNode</span></span>
```
Get-AzureRmServerManagementSession [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="994eb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="994eb-108">DESCRIPTION</span></span>
<span data-ttu-id="994eb-109">Il cmdlet **Get-AzureRmServerManagementSession** ottiene una singola sessione di gestione di Azure server.</span><span class="sxs-lookup"><span data-stu-id="994eb-109">The **Get-AzureRmServerManagementSession** cmdlet gets a single Azure Server Management session.</span></span>

## <span data-ttu-id="994eb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="994eb-110">EXAMPLES</span></span>

## <span data-ttu-id="994eb-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="994eb-111">PARAMETERS</span></span>

### <span data-ttu-id="994eb-112">-Node</span><span class="sxs-lookup"><span data-stu-id="994eb-112">-Node</span></span>
<span data-ttu-id="994eb-113">Specifica un oggetto **node** esistente usato per ottenere i parametri *ResourceGroupName* e *NodeName* .</span><span class="sxs-lookup"><span data-stu-id="994eb-113">Specifies an existing **Node** object that is used to get the *ResourceGroupName* and the *NodeName* parameters.</span></span>
<span data-ttu-id="994eb-114">Devi anche specificare un valore per il parametro *sessionname* .</span><span class="sxs-lookup"><span data-stu-id="994eb-114">You must also specify a value for the *SessionName* parameter.</span></span>

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

### <span data-ttu-id="994eb-115">-NodeName</span><span class="sxs-lookup"><span data-stu-id="994eb-115">-NodeName</span></span>
<span data-ttu-id="994eb-116">Specifica il nome del nodo in cui si trova la sessione.</span><span class="sxs-lookup"><span data-stu-id="994eb-116">Specifies the name of the node where the session is located.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="994eb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="994eb-117">-ResourceGroupName</span></span>
<span data-ttu-id="994eb-118">Specifica il nome del gruppo di risorse per cui questo cmdlet recupera la sessione.</span><span class="sxs-lookup"><span data-stu-id="994eb-118">Specifies the name of the resource group for which this cmdlet gets the retrieve the session.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="994eb-119">-Sessione</span><span class="sxs-lookup"><span data-stu-id="994eb-119">-Session</span></span>
<span data-ttu-id="994eb-120">Specifica un oggetto **Session** esistente usato per ottenere il *ResourceGroupName* , il *NodeName* e i parametri *sessionname* .</span><span class="sxs-lookup"><span data-stu-id="994eb-120">Specifies an existing **Session** object that is used to get the *ResourceGroupName* , the *NodeName* , and the *SessionName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Session
Parameter Sets: BySession
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="994eb-121">-Sessionname</span><span class="sxs-lookup"><span data-stu-id="994eb-121">-SessionName</span></span>
<span data-ttu-id="994eb-122">Specifica il nome della sessione in cui viene ottenuto questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="994eb-122">Specifies the name of the session in which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BySession
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="994eb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="994eb-123">-DefaultProfile</span></span>
<span data-ttu-id="994eb-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="994eb-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="994eb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="994eb-125">CommonParameters</span></span>
<span data-ttu-id="994eb-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="994eb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="994eb-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="994eb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="994eb-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="994eb-128">INPUTS</span></span>

### <span data-ttu-id="994eb-129">Nodo</span><span class="sxs-lookup"><span data-stu-id="994eb-129">Node</span></span>
<span data-ttu-id="994eb-130">Il parametro "node" accetta il valore di tipo "node" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="994eb-130">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

### <span data-ttu-id="994eb-131">Sessione</span><span class="sxs-lookup"><span data-stu-id="994eb-131">Session</span></span>
<span data-ttu-id="994eb-132">Il parametro "Session" accetta il valore di tipo "Session" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="994eb-132">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="994eb-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="994eb-133">OUTPUTS</span></span>

### <span data-ttu-id="994eb-134">Microsoft. Azure. Commands. ServerManagement. Model. Session</span><span class="sxs-lookup"><span data-stu-id="994eb-134">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="994eb-135">Note</span><span class="sxs-lookup"><span data-stu-id="994eb-135">NOTES</span></span>

## <span data-ttu-id="994eb-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="994eb-136">RELATED LINKS</span></span>

[<span data-ttu-id="994eb-137">Cmdlet di gestione di Azure server</span><span class="sxs-lookup"><span data-stu-id="994eb-137">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


