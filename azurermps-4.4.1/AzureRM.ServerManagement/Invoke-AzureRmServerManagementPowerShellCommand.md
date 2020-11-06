---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 1EA5F348-5EF4-4056-BA06-7B95E12E329D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
ms.openlocfilehash: 5acd510118f2be26ba09f3e0fefbc9b0c80aae02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516040"
---
# <span data-ttu-id="ed8b2-101">Invoke-AzureRmServerManagementPowerShellCommand</span><span class="sxs-lookup"><span data-stu-id="ed8b2-101">Invoke-AzureRmServerManagementPowerShellCommand</span></span>

## <span data-ttu-id="ed8b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed8b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ed8b2-103">Esegue un blocco di script di Windows PowerShell in un nodo.</span><span class="sxs-lookup"><span data-stu-id="ed8b2-103">Executes a Windows PowerShell script block on a node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed8b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed8b2-104">SYNTAX</span></span>

### <span data-ttu-id="ed8b2-105">ByName</span><span class="sxs-lookup"><span data-stu-id="ed8b2-105">ByName</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-Command] <ScriptBlock> [-PowerShellSessionName <String>] [-RawOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed8b2-106">BySession</span><span class="sxs-lookup"><span data-stu-id="ed8b2-106">BySession</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-Session] <Session> [-Command] <ScriptBlock>
 [-PowerShellSessionName <String>] [-RawOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed8b2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed8b2-107">DESCRIPTION</span></span>
<span data-ttu-id="ed8b2-108">Il cmdlet **Invoke-AzureRmServerManagementPowerShellCommand** esegue un blocco di script di Windows PowerShell in un nodo gestito da un gateway di gestione di Azure server.</span><span class="sxs-lookup"><span data-stu-id="ed8b2-108">The **Invoke-AzureRmServerManagementPowerShellCommand** cmdlet executes a Windows PowerShell script block on a node managed by an Azure Server Management Gateway.</span></span>

## <span data-ttu-id="ed8b2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed8b2-109">EXAMPLES</span></span>

## <span data-ttu-id="ed8b2-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed8b2-110">PARAMETERS</span></span>

### <span data-ttu-id="ed8b2-111">-Comando</span><span class="sxs-lookup"><span data-stu-id="ed8b2-111">-Command</span></span>
<span data-ttu-id="ed8b2-112">Specifica il blocco di script da eseguire nel nodo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ed8b2-112">Specifies the script block to run on the target node.</span></span>

```yaml
Type: System.Management.Automation.ScriptBlock
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8b2-113">-NodeName</span><span class="sxs-lookup"><span data-stu-id="ed8b2-113">-NodeName</span></span>
<span data-ttu-id="ed8b2-114">Specifica il nome del nodo in cui eseguire il blocco di script.</span><span class="sxs-lookup"><span data-stu-id="ed8b2-114">Specifies the name of the node to run the script block on.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8b2-115">-PowerShellSessionName</span><span class="sxs-lookup"><span data-stu-id="ed8b2-115">-PowerShellSessionName</span></span>
<span data-ttu-id="ed8b2-116">Specifica il nome dello spazio di esecuzione di Windows PowerShell nel nodo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ed8b2-116">Specifies the name of the Windows PowerShell run space on the target node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8b2-117">-RawOutput</span><span class="sxs-lookup"><span data-stu-id="ed8b2-117">-RawOutput</span></span>
<span data-ttu-id="ed8b2-118">Indica che il cmdlet restituisce l'oggetto completo che contiene l'output del nodo.</span><span class="sxs-lookup"><span data-stu-id="ed8b2-118">Indicates that the cmdlet returns the complete object that contains the output from the node.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8b2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed8b2-119">-ResourceGroupName</span></span>
<span data-ttu-id="ed8b2-120">Specifica il nome del gruppo di risorse a cui appartiene il nodo.</span><span class="sxs-lookup"><span data-stu-id="ed8b2-120">Specifies the name of the resource group that the node belongs to.</span></span>

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

### <span data-ttu-id="ed8b2-121">-Sessione</span><span class="sxs-lookup"><span data-stu-id="ed8b2-121">-Session</span></span>
<span data-ttu-id="ed8b2-122">Specifica l'oggetto **Session** usato da questo cmdlet per la connessione al nodo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="ed8b2-122">Specifies the **Session** object that this cmdlet uses to connect to the target node.</span></span>

<span data-ttu-id="ed8b2-123">Questo parametro può essere specificato al posto dei parametri *ResourceGroupName* , *NodeName* , *sessionname* e *PowerShellSessionName* .</span><span class="sxs-lookup"><span data-stu-id="ed8b2-123">This parameter may be specified instead of the *ResourceGroupName* , *NodeName* , *SessionName* , and *PowerShellSessionName* parameters.</span></span>

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

### <span data-ttu-id="ed8b2-124">-Sessionname</span><span class="sxs-lookup"><span data-stu-id="ed8b2-124">-SessionName</span></span>
<span data-ttu-id="ed8b2-125">Specifica il nome della sessione per la gestione del nodo.</span><span class="sxs-lookup"><span data-stu-id="ed8b2-125">Specifies the name of the session to manage the node.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8b2-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed8b2-126">-DefaultProfile</span></span>
<span data-ttu-id="ed8b2-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed8b2-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed8b2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed8b2-128">CommonParameters</span></span>
<span data-ttu-id="ed8b2-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed8b2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed8b2-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed8b2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed8b2-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed8b2-131">INPUTS</span></span>

### <span data-ttu-id="ed8b2-132">Sessione</span><span class="sxs-lookup"><span data-stu-id="ed8b2-132">Session</span></span>
<span data-ttu-id="ed8b2-133">Il parametro "Session" accetta il valore di tipo "Session" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ed8b2-133">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="ed8b2-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed8b2-134">OUTPUTS</span></span>

### <span data-ttu-id="ed8b2-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="ed8b2-135">System.Object</span></span>

## <span data-ttu-id="ed8b2-136">Note</span><span class="sxs-lookup"><span data-stu-id="ed8b2-136">NOTES</span></span>

## <span data-ttu-id="ed8b2-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed8b2-137">RELATED LINKS</span></span>

[<span data-ttu-id="ed8b2-138">Cmdlet di gestione di Azure server</span><span class="sxs-lookup"><span data-stu-id="ed8b2-138">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


