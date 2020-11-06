---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: CEA14FAB-4B57-48F2-938C-E3AD4AAAE753
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementNode.md
ms.openlocfilehash: 498be36141d1a44d33cdcb351b92d5b6908071c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507963"
---
# <span data-ttu-id="cc677-101">New-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="cc677-101">New-AzureRmServerManagementNode</span></span>

## <span data-ttu-id="cc677-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cc677-102">SYNOPSIS</span></span>
<span data-ttu-id="cc677-103">Crea un nodo di gestione del server.</span><span class="sxs-lookup"><span data-stu-id="cc677-103">Creates a Server Management node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc677-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cc677-104">SYNTAX</span></span>

### <span data-ttu-id="cc677-105">ByName</span><span class="sxs-lookup"><span data-stu-id="cc677-105">ByName</span></span>
```
New-AzureRmServerManagementNode [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 -NodeName <String> [-ComputerName <String>] -Credential <PSCredential> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cc677-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="cc677-106">ByObject</span></span>
```
New-AzureRmServerManagementNode [-Gateway] <Gateway> -NodeName <String> [-ComputerName <String>]
 -Credential <PSCredential> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cc677-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cc677-107">DESCRIPTION</span></span>
<span data-ttu-id="cc677-108">Il cmdlet **New-AzureRmServerManagementNode** crea un nodo di gestione di Azure server.</span><span class="sxs-lookup"><span data-stu-id="cc677-108">The **New-AzureRmServerManagementNode** cmdlet creates an Azure Server Management node.</span></span>

## <span data-ttu-id="cc677-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cc677-109">EXAMPLES</span></span>

## <span data-ttu-id="cc677-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cc677-110">PARAMETERS</span></span>

### <span data-ttu-id="cc677-111">-Nomecomputer</span><span class="sxs-lookup"><span data-stu-id="cc677-111">-ComputerName</span></span>
<span data-ttu-id="cc677-112">Specifica il nome del computer che viene gestito.</span><span class="sxs-lookup"><span data-stu-id="cc677-112">Specifies the computer name of the computer that is being managed.</span></span>

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

### <span data-ttu-id="cc677-113">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="cc677-113">-Credential</span></span>
<span data-ttu-id="cc677-114">Specifica un oggetto **PSCredential** per la connessione al nodo di gestione del server.</span><span class="sxs-lookup"><span data-stu-id="cc677-114">Specifies a **PSCredential** object for the connection to the Server Management Node.</span></span>
<span data-ttu-id="cc677-115">Per ottenere un oggetto Credential, usa il cmdlet Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="cc677-115">To obtain a credential object, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="cc677-116">Per altre informazioni, digitare `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="cc677-116">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc677-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc677-117">-DefaultProfile</span></span>
<span data-ttu-id="cc677-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cc677-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc677-119">-Gateway</span><span class="sxs-lookup"><span data-stu-id="cc677-119">-Gateway</span></span>
<span data-ttu-id="cc677-120">Specifica il gateway che gestisce il nodo.</span><span class="sxs-lookup"><span data-stu-id="cc677-120">Specifies the gateway that manages the node.</span></span>

<span data-ttu-id="cc677-121">Questo parametro può essere usato al posto dei parametri *ResourceGroupName* , *GatewayName* e *location* .</span><span class="sxs-lookup"><span data-stu-id="cc677-121">This parameter can be used instead of the *ResourceGroupName* , *GatewayName* , and *Location* parameters.</span></span>

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

### <span data-ttu-id="cc677-122">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="cc677-122">-GatewayName</span></span>
<span data-ttu-id="cc677-123">Specifica il nome del gateway che accede al nodo.</span><span class="sxs-lookup"><span data-stu-id="cc677-123">Specifies the name of the gateway that accesses the node.</span></span>

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

### <span data-ttu-id="cc677-124">-Posizione</span><span class="sxs-lookup"><span data-stu-id="cc677-124">-Location</span></span>
<span data-ttu-id="cc677-125">Specifica la posizione in cui questo cmdlet crea il nodo.</span><span class="sxs-lookup"><span data-stu-id="cc677-125">Specifies the location in which this cmdlet creates the node.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc677-126">-NodeName</span><span class="sxs-lookup"><span data-stu-id="cc677-126">-NodeName</span></span>
<span data-ttu-id="cc677-127">Specifica il nome del nodo.</span><span class="sxs-lookup"><span data-stu-id="cc677-127">Specifies the name of the node.</span></span>

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

### <span data-ttu-id="cc677-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc677-128">-ResourceGroupName</span></span>
<span data-ttu-id="cc677-129">Specifica il nome del gruppo di risorse in cui questo cmdlet crea il nodo.</span><span class="sxs-lookup"><span data-stu-id="cc677-129">Specifies the name of the resource group in which this cmdlet creates the node.</span></span>

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

### <span data-ttu-id="cc677-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="cc677-130">-Tag</span></span>
<span data-ttu-id="cc677-131">Coppie chiave/valore associate all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="cc677-131">Key/value pairs associated with the object.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc677-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc677-132">CommonParameters</span></span>
<span data-ttu-id="cc677-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc677-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc677-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc677-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc677-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cc677-135">INPUTS</span></span>

### <span data-ttu-id="cc677-136">Gateway</span><span class="sxs-lookup"><span data-stu-id="cc677-136">Gateway</span></span>
<span data-ttu-id="cc677-137">Il parametro "gateway" accetta il valore di tipo "gateway" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="cc677-137">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="cc677-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cc677-138">OUTPUTS</span></span>

### <span data-ttu-id="cc677-139">Microsoft. Azure. Commands. ServerManagement. Model. Node</span><span class="sxs-lookup"><span data-stu-id="cc677-139">Microsoft.Azure.Commands.ServerManagement.Model.Node</span></span>

## <span data-ttu-id="cc677-140">Note</span><span class="sxs-lookup"><span data-stu-id="cc677-140">NOTES</span></span>

## <span data-ttu-id="cc677-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cc677-141">RELATED LINKS</span></span>

[<span data-ttu-id="cc677-142">Get-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="cc677-142">Get-AzureRmServerManagementNode</span></span>](./Get-AzureRmServerManagementNode.md)

[<span data-ttu-id="cc677-143">Remove-AzureRmServerManagementNode</span><span class="sxs-lookup"><span data-stu-id="cc677-143">Remove-AzureRmServerManagementNode</span></span>](./Remove-AzureRmServerManagementNode.md)


