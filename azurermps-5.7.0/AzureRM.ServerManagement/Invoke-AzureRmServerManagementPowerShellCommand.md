---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1EA5F348-5EF4-4056-BA06-7B95E12E329D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/invoke-azurermservermanagementpowershellcommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
ms.openlocfilehash: d4720a1159d55064a007a97df7233853200f1295
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512308"
---
# <span data-ttu-id="7ead4-101">Invoke-AzureRmServerManagementPowerShellCommand</span><span class="sxs-lookup"><span data-stu-id="7ead4-101">Invoke-AzureRmServerManagementPowerShellCommand</span></span>

## <span data-ttu-id="7ead4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7ead4-102">SYNOPSIS</span></span>
<span data-ttu-id="7ead4-103">Esegue un blocco di script di Windows PowerShell in un nodo.</span><span class="sxs-lookup"><span data-stu-id="7ead4-103">Executes a Windows PowerShell script block on a node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ead4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ead4-104">SYNTAX</span></span>

### <span data-ttu-id="7ead4-105">ByName</span><span class="sxs-lookup"><span data-stu-id="7ead4-105">ByName</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-Command] <ScriptBlock> [-PowerShellSessionName <String>] [-RawOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ead4-106">BySession</span><span class="sxs-lookup"><span data-stu-id="7ead4-106">BySession</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-Session] <Session> [-Command] <ScriptBlock>
 [-PowerShellSessionName <String>] [-RawOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ead4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ead4-107">DESCRIPTION</span></span>
<span data-ttu-id="7ead4-108">Il cmdlet **Invoke-AzureRmServerManagementPowerShellCommand** esegue un blocco di script di Windows PowerShell in un nodo gestito da un gateway di gestione di Azure server.</span><span class="sxs-lookup"><span data-stu-id="7ead4-108">The **Invoke-AzureRmServerManagementPowerShellCommand** cmdlet executes a Windows PowerShell script block on a node managed by an Azure Server Management Gateway.</span></span>

## <span data-ttu-id="7ead4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ead4-109">EXAMPLES</span></span>

## <span data-ttu-id="7ead4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7ead4-110">PARAMETERS</span></span>

### <span data-ttu-id="7ead4-111">-Comando</span><span class="sxs-lookup"><span data-stu-id="7ead4-111">-Command</span></span>
<span data-ttu-id="7ead4-112">Specifica il blocco di script da eseguire nel nodo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7ead4-112">Specifies the script block to run on the target node.</span></span>

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ead4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ead4-113">-DefaultProfile</span></span>
<span data-ttu-id="7ead4-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7ead4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ead4-115">-NodeName</span><span class="sxs-lookup"><span data-stu-id="7ead4-115">-NodeName</span></span>
<span data-ttu-id="7ead4-116">Specifica il nome del nodo in cui eseguire il blocco di script.</span><span class="sxs-lookup"><span data-stu-id="7ead4-116">Specifies the name of the node to run the script block on.</span></span>

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

### <span data-ttu-id="7ead4-117">-PowerShellSessionName</span><span class="sxs-lookup"><span data-stu-id="7ead4-117">-PowerShellSessionName</span></span>
<span data-ttu-id="7ead4-118">Specifica il nome dello spazio di esecuzione di Windows PowerShell nel nodo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7ead4-118">Specifies the name of the Windows PowerShell run space on the target node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ead4-119">-RawOutput</span><span class="sxs-lookup"><span data-stu-id="7ead4-119">-RawOutput</span></span>
<span data-ttu-id="7ead4-120">Indica che il cmdlet restituisce l'oggetto completo che contiene l'output del nodo.</span><span class="sxs-lookup"><span data-stu-id="7ead4-120">Indicates that the cmdlet returns the complete object that contains the output from the node.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ead4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ead4-121">-ResourceGroupName</span></span>
<span data-ttu-id="7ead4-122">Specifica il nome del gruppo di risorse a cui appartiene il nodo.</span><span class="sxs-lookup"><span data-stu-id="7ead4-122">Specifies the name of the resource group that the node belongs to.</span></span>

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

### <span data-ttu-id="7ead4-123">-Sessione</span><span class="sxs-lookup"><span data-stu-id="7ead4-123">-Session</span></span>
<span data-ttu-id="7ead4-124">Specifica l'oggetto **Session** usato da questo cmdlet per la connessione al nodo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7ead4-124">Specifies the **Session** object that this cmdlet uses to connect to the target node.</span></span>

<span data-ttu-id="7ead4-125">Questo parametro può essere specificato al posto dei parametri *ResourceGroupName* , *NodeName* , *sessionname* e *PowerShellSessionName* .</span><span class="sxs-lookup"><span data-stu-id="7ead4-125">This parameter may be specified instead of the *ResourceGroupName* , *NodeName* , *SessionName* , and *PowerShellSessionName* parameters.</span></span>

```yaml
Type: Session
Parameter Sets: BySession
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ead4-126">-Sessionname</span><span class="sxs-lookup"><span data-stu-id="7ead4-126">-SessionName</span></span>
<span data-ttu-id="7ead4-127">Specifica il nome della sessione per la gestione del nodo.</span><span class="sxs-lookup"><span data-stu-id="7ead4-127">Specifies the name of the session to manage the node.</span></span>

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

### <span data-ttu-id="7ead4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ead4-128">CommonParameters</span></span>
<span data-ttu-id="7ead4-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ead4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ead4-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ead4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ead4-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7ead4-131">INPUTS</span></span>

### <span data-ttu-id="7ead4-132">Sessione</span><span class="sxs-lookup"><span data-stu-id="7ead4-132">Session</span></span>
<span data-ttu-id="7ead4-133">Il parametro "Session" accetta il valore di tipo "Session" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7ead4-133">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="7ead4-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ead4-134">OUTPUTS</span></span>

### <span data-ttu-id="7ead4-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="7ead4-135">System.Object</span></span>

## <span data-ttu-id="7ead4-136">Note</span><span class="sxs-lookup"><span data-stu-id="7ead4-136">NOTES</span></span>

## <span data-ttu-id="7ead4-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ead4-137">RELATED LINKS</span></span>

[<span data-ttu-id="7ead4-138">Cmdlet di gestione di Azure server</span><span class="sxs-lookup"><span data-stu-id="7ead4-138">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


