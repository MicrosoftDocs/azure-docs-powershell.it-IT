---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Export-AzureAnalysisServicesInstanceLog.md
ms.openlocfilehash: 5354737602f168245d6c4c8dca560698fa6cfac2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688533"
---
# <span data-ttu-id="777d3-101">Export-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="777d3-101">Export-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="777d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="777d3-102">SYNOPSIS</span></span>
<span data-ttu-id="777d3-103">Esporta un log da un'istanza del server di Analysis Services nell'ambiente attualmente connesso, come specificato nel comando Add-AzureAnalysisServicesAccount</span><span class="sxs-lookup"><span data-stu-id="777d3-103">Exports a log from an instance of Analysis Services server in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="777d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="777d3-104">SYNTAX</span></span>

```
Export-AzureAnalysisServicesInstanceLog [-Instance] <String> [-OutputPath] <String> [-WhatIf] [-Force]
```

## <span data-ttu-id="777d3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="777d3-105">DESCRIPTION</span></span>
<span data-ttu-id="777d3-106">Il cmdlet Export-AzureAnalysisServicesInstance Esporta il log da un'istanza di Azure Analysis Services server a file</span><span class="sxs-lookup"><span data-stu-id="777d3-106">The Export-AzureAnalysisServicesInstance cmdlet exports log from an instance of Azure Analysis Services server to file</span></span>

## <span data-ttu-id="777d3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="777d3-107">EXAMPLES</span></span>

### <span data-ttu-id="777d3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="777d3-108">Example 1</span></span>
```
PS C:\>Export-AzureAnalysisServicesInstanceLog -Instance testserver -OuptutPath C:\path\to\log\testserver.log
```

<span data-ttu-id="777d3-109">Questo comando esporterà il log dal server "TestServer" nell'ambiente specificato nel comando Add-AzureAnalysisServicesAccount e lo salverà in file specificato in OutputPath "C:\path\to\log\testserver.log"</span><span class="sxs-lookup"><span data-stu-id="777d3-109">This command will export log from the server 'testserver' in the environment specified in the Add-AzureAnalysisServicesAccount command and save it to file specified in OutputPath 'C:\path\to\log\testserver.log'</span></span>

## <span data-ttu-id="777d3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="777d3-110">PARAMETERS</span></span>

### <span data-ttu-id="777d3-111">-Instance</span><span class="sxs-lookup"><span data-stu-id="777d3-111">-Instance</span></span>
<span data-ttu-id="777d3-112">Nome dell'istanza del server Analysis Services</span><span class="sxs-lookup"><span data-stu-id="777d3-112">Name of the Analysis Services server instance</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="777d3-113">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="777d3-113">-OutputPath</span></span>
<span data-ttu-id="777d3-114">Percorso di output del file per esportare il log</span><span class="sxs-lookup"><span data-stu-id="777d3-114">Output path to file to export log</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="777d3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="777d3-115">-Force</span></span>
<span data-ttu-id="777d3-116">Sovrascrivere il file se esiste senza chiedere</span><span class="sxs-lookup"><span data-stu-id="777d3-116">Overwrite file if exists without asking</span></span>

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

## <span data-ttu-id="777d3-117">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="777d3-117">INPUTS</span></span>

## <span data-ttu-id="777d3-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="777d3-118">OUTPUTS</span></span>

## <span data-ttu-id="777d3-119">Note</span><span class="sxs-lookup"><span data-stu-id="777d3-119">NOTES</span></span>
<span data-ttu-id="777d3-120">Alias: Export-AzureAsInstanceLog</span><span class="sxs-lookup"><span data-stu-id="777d3-120">Alias: Export-AzureAsInstanceLog</span></span>

## <span data-ttu-id="777d3-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="777d3-121">RELATED LINKS</span></span>

