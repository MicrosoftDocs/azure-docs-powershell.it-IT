---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolgeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolGeoBackup.md
ms.openlocfilehash: d1c0b6439b148d51506861a6bfffc6a6681343ef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957869"
---
# <span data-ttu-id="7d8ad-101">Get-AzSynapseSqlPoolGeoBackup</span><span class="sxs-lookup"><span data-stu-id="7d8ad-101">Get-AzSynapseSqlPoolGeoBackup</span></span>

## <span data-ttu-id="7d8ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d8ad-102">SYNOPSIS</span></span>
<span data-ttu-id="7d8ad-103">Ottiene un backup geo-ridondante di un pool Sql.</span><span class="sxs-lookup"><span data-stu-id="7d8ad-103">Gets a geo-redundant backup of a Sql Pool.</span></span>

## <span data-ttu-id="7d8ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d8ad-104">SYNTAX</span></span>

### <span data-ttu-id="7d8ad-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7d8ad-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d8ad-106">SqlPoolGeoBackupResourceId</span><span class="sxs-lookup"><span data-stu-id="7d8ad-106">SqlPoolGeoBackupResourceId</span></span>
```
Get-AzSynapseSqlPoolGeoBackup [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d8ad-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7d8ad-107">DESCRIPTION</span></span>
<span data-ttu-id="7d8ad-108">Il cmdlet **Get-AzSynapseSqlPoolGeoBackup** ottiene un backup geo-ridondante specificato di un pool di SQL o di tutti i backup geo-ridondanti disponibili in un'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="7d8ad-108">The **Get-AzSynapseSqlPoolGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL Pool or all available geo-redundant backups on a specified workspace.</span></span>
<span data-ttu-id="7d8ad-109">Un backup geo-ridondante è una risorsa ripristinabile che usa file di dati da una posizione geografica separata.</span><span class="sxs-lookup"><span data-stu-id="7d8ad-109">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="7d8ad-110">È possibile usare Geo-Restore per ripristinare un backup geo-ridondante in caso di un'interruzione regionale e ripristinare il pool sql in una nuova area geografica.</span><span class="sxs-lookup"><span data-stu-id="7d8ad-110">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your Sql Pool to a new region.</span></span>

## <span data-ttu-id="7d8ad-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d8ad-111">EXAMPLES</span></span>

### <span data-ttu-id="7d8ad-112">Esempio 1: Ottenere un backup geo-ridondante specificato</span><span class="sxs-lookup"><span data-stu-id="7d8ad-112">Example 1: Get a specified geo-redundant backup</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName ContosoResourceGroup -WorkspaceName "ContosoWorkspace" -Name "ContosoSqlPool"
```
<span data-ttu-id="7d8ad-113">Il cmdlet recupera il backup geografico per un pool SQL.</span><span class="sxs-lookup"><span data-stu-id="7d8ad-113">The cmdlet retrieves Geo Backup for a sql pool.</span></span>

### <span data-ttu-id="7d8ad-114">Esempio 2: Ottenere tutti i backup geo-ridondanti in un'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="7d8ad-114">Example 2: Get all geo-redundant backups on a workspace</span></span>
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```
<span data-ttu-id="7d8ad-115">Questo comando recupera tutti i backup geo-ridondanti disponibili in un'area di lavoro specificata.</span><span class="sxs-lookup"><span data-stu-id="7d8ad-115">This command gets all available geo-redundant backups on a specified workspace.</span></span>

### <span data-ttu-id="7d8ad-116">Esempio 3: Ottenere tutti i backup geo-ridondanti in un'area di lavoro usando i filtri</span><span class="sxs-lookup"><span data-stu-id="7d8ad-116">Example 3: Get all geo-redundant backups on a workspace using filtering</span></span>
```
PS C:\>Get-AzSynapseSqlPoolGeoBackup -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -Name "Contoso*"
```
<span data-ttu-id="7d8ad-117">Questo comando recupera tutti i backup geo-ridondanti disponibili in un'area di lavoro specificata che inizia con "Contoso".</span><span class="sxs-lookup"><span data-stu-id="7d8ad-117">This command gets all available geo-redundant backups on a specified workspace that start with "Contoso".</span></span>

## <span data-ttu-id="7d8ad-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d8ad-118">PARAMETERS</span></span>

### <span data-ttu-id="7d8ad-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d8ad-119">-DefaultProfile</span></span>
<span data-ttu-id="7d8ad-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d8ad-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d8ad-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7d8ad-121">-Name</span></span>
<span data-ttu-id="7d8ad-122">Pool Synapse Sql.</span><span class="sxs-lookup"><span data-stu-id="7d8ad-122">The Synapse Sql pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: The Synapse Sql pool.

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d8ad-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d8ad-123">-ResourceId</span></span>
<span data-ttu-id="7d8ad-124">Immettere un ID risorsa di backup geografico del pool Sql.</span><span class="sxs-lookup"><span data-stu-id="7d8ad-124">Input a Sql Pool Geo Backup Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolGeoBackupResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d8ad-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d8ad-125">-ResourceGroupName</span></span>
<span data-ttu-id="7d8ad-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7d8ad-126">Resource group name.</span></span>

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

### <span data-ttu-id="7d8ad-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7d8ad-127">-WorkspaceName</span></span>
<span data-ttu-id="7d8ad-128">Nome dell'area di lavoro Synapse.</span><span class="sxs-lookup"><span data-stu-id="7d8ad-128">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="7d8ad-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d8ad-129">CommonParameters</span></span>
<span data-ttu-id="7d8ad-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d8ad-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d8ad-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7d8ad-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d8ad-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="7d8ad-132">INPUTS</span></span>

### <span data-ttu-id="7d8ad-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7d8ad-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7d8ad-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7d8ad-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseResourceGroup</span></span>

## <span data-ttu-id="7d8ad-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d8ad-135">OUTPUTS</span></span>

### <span data-ttu-id="7d8ad-136">Microsoft.Azure.Commands.Synapse.Models.PSBackupModel</span><span class="sxs-lookup"><span data-stu-id="7d8ad-136">Microsoft.Azure.Commands.Synapse.Models.PSBackupModel</span></span>

## <span data-ttu-id="7d8ad-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="7d8ad-137">NOTES</span></span>

## <span data-ttu-id="7d8ad-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d8ad-138">RELATED LINKS</span></span>
