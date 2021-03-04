---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsedroppedsqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDroppedSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseDroppedSqlPool.md
ms.openlocfilehash: 26e4e5c77913f01b8a7097f6baebd68977ceed22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981837"
---
# <span data-ttu-id="8634b-101">Get-AzSynapseDroppedSqlPool</span><span class="sxs-lookup"><span data-stu-id="8634b-101">Get-AzSynapseDroppedSqlPool</span></span>

## <span data-ttu-id="8634b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8634b-102">SYNOPSIS</span></span>
<span data-ttu-id="8634b-103">Ottiene un backup del pool Sql eliminato di un pool Sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="8634b-103">Gets a dropped Sql pool backup of a Synapse Sql Pool.</span></span>

## <span data-ttu-id="8634b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8634b-104">SYNTAX</span></span>

### <span data-ttu-id="8634b-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8634b-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseDroppedSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8634b-106">DroppedSqlPoolResourceId</span><span class="sxs-lookup"><span data-stu-id="8634b-106">DroppedSqlPoolResourceId</span></span>
```
Get-AzSynapseDroppedSqlPool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8634b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8634b-107">DESCRIPTION</span></span>
<span data-ttu-id="8634b-108">Il cmdlet **Get-AzSynapseDroppedSqlPool** ottiene un backup specificato del pool SQL eliminato che è possibile ripristinare o tutti i backup eliminati che è possibile ripristinare in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8634b-108">The **Get-AzSynapseDroppedSqlPool** cmdlet gets a specified deleted SQL pool backup that you can restore, or all deleted backups that you can restore in a workspace.</span></span> 


## <span data-ttu-id="8634b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8634b-109">EXAMPLES</span></span>

### <span data-ttu-id="8634b-110">Esempio 1: Ottenere uno specificato pool sql eliminato da un pool SQL</span><span class="sxs-lookup"><span data-stu-id="8634b-110">Example 1: Get a specified dropped sqlpools from a sql pool</span></span>
```powershell
PS C:\> Get-AzSynapseDroppedSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name "ContosoSqlPool"
```
<span data-ttu-id="8634b-111">Il cmdlet recupera i pool sql eliminati per un pool di SQL.</span><span class="sxs-lookup"><span data-stu-id="8634b-111">The cmdlet retrieves dropped sqlpools for a sql pool.</span></span>

### <span data-ttu-id="8634b-112">Esempio 2: Ottenere tutto il pool sql eliminato in un'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="8634b-112">Example 2: Get all dropped sqlpool on a workspace</span></span>
```
PS C:\>Get-AzSynapseDroppedSqlPool -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```
<span data-ttu-id="8634b-113">Questo comando consente di ottenere tutto il pool sql eliminato disponibile in un'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="8634b-113">This command gets all available dropped sqlpool on a specified workspace.</span></span>

## <span data-ttu-id="8634b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8634b-114">PARAMETERS</span></span>

### <span data-ttu-id="8634b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8634b-115">-DefaultProfile</span></span>
<span data-ttu-id="8634b-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8634b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8634b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8634b-117">-Name</span></span>
<span data-ttu-id="8634b-118">Pool Synapse Sql.</span><span class="sxs-lookup"><span data-stu-id="8634b-118">The Synapse Sql pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: AzSynapseDroppedSqlPool

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8634b-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8634b-119">-ResourceId</span></span>
<span data-ttu-id="8634b-120">Immettere un ID di risorsa pool Sql eliminato.</span><span class="sxs-lookup"><span data-stu-id="8634b-120">Input a Dropped Sql Pool Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: DroppedSqlPoolResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8634b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8634b-121">-ResourceGroupName</span></span>
<span data-ttu-id="8634b-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8634b-122">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8634b-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8634b-123">-WorkspaceName</span></span>
<span data-ttu-id="8634b-124">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="8634b-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8634b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8634b-125">CommonParameters</span></span>
<span data-ttu-id="8634b-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8634b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8634b-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8634b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8634b-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="8634b-128">INPUTS</span></span>

### <span data-ttu-id="8634b-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="8634b-129">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="8634b-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8634b-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span></span>

## <span data-ttu-id="8634b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8634b-131">OUTPUTS</span></span>

### <span data-ttu-id="8634b-132">Microsoft.Azure.Commands.Synapse.Models.PSDroppedSqlPoolBackupModel</span><span class="sxs-lookup"><span data-stu-id="8634b-132">Microsoft.Azure.Commands.Synapse.Models.PSDroppedSqlPoolBackupModel</span></span>

## <span data-ttu-id="8634b-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="8634b-133">NOTES</span></span>

## <span data-ttu-id="8634b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8634b-134">RELATED LINKS</span></span>
