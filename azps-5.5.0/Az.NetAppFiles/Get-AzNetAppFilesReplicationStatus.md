---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesreplicationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
ms.openlocfilehash: e59ce4f5e3b0f1b07744e0754cf0e1cae3de7da6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192078"
---
# <span data-ttu-id="c5503-101">Get-AzNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="c5503-101">Get-AzNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="c5503-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5503-102">SYNOPSIS</span></span>
<span data-ttu-id="c5503-103">Ottenere lo stato della replica</span><span class="sxs-lookup"><span data-stu-id="c5503-103">Get the status of the replication</span></span>

## <span data-ttu-id="c5503-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c5503-104">SYNTAX</span></span>

### <span data-ttu-id="c5503-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c5503-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5503-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5503-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5503-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5503-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5503-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c5503-108">DESCRIPTION</span></span>
<span data-ttu-id="c5503-109">Ottenere lo stato della replica</span><span class="sxs-lookup"><span data-stu-id="c5503-109">Get the status of the replication</span></span>

## <span data-ttu-id="c5503-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c5503-110">EXAMPLES</span></span>

### <span data-ttu-id="c5503-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c5503-111">Example 1</span></span>
```powershell
PS C:\> Get-AnfReplicationStatus -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolName "MyDestinationPool" -VolumeName "MyVol"

Output:

Healthy            : true
RelationshipStatus : Idle
MirrorState        : Mirrored
TotalProgress      : 1024
ErrorMessage       :
```

<span data-ttu-id="c5503-112">Questo comando ottiene lo stato di replica su MyVol</span><span class="sxs-lookup"><span data-stu-id="c5503-112">This command gets the status of replication on MyVol</span></span>

## <span data-ttu-id="c5503-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5503-113">PARAMETERS</span></span>

### <span data-ttu-id="c5503-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c5503-114">-AccountName</span></span>
<span data-ttu-id="c5503-115">Nome dell'account ANF del volume di destinazione della replica</span><span class="sxs-lookup"><span data-stu-id="c5503-115">The name of the ANF account of the replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5503-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5503-116">-DefaultProfile</span></span>
<span data-ttu-id="c5503-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c5503-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5503-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5503-118">-InputObject</span></span>
<span data-ttu-id="c5503-119">Oggetto volume di destinazione della replica ANF per ottenere lo stato di replica</span><span class="sxs-lookup"><span data-stu-id="c5503-119">The ANF replication destination volume object to get replication status</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5503-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c5503-120">-Name</span></span>
<span data-ttu-id="c5503-121">Nome del volume di destinazione della replica ANF</span><span class="sxs-lookup"><span data-stu-id="c5503-121">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5503-122">-PoolName</span><span class="sxs-lookup"><span data-stu-id="c5503-122">-PoolName</span></span>
<span data-ttu-id="c5503-123">Nome del pool ANF del volume di destinazione della replica</span><span class="sxs-lookup"><span data-stu-id="c5503-123">The name of the ANF pool of the replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5503-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5503-124">-ResourceGroupName</span></span>
<span data-ttu-id="c5503-125">Gruppo di risorse del volume di destinazione della replica ANF</span><span class="sxs-lookup"><span data-stu-id="c5503-125">The resource group of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5503-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5503-126">-ResourceId</span></span>
<span data-ttu-id="c5503-127">ID risorsa del volume di destinazione della replica ANF</span><span class="sxs-lookup"><span data-stu-id="c5503-127">The resource id of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5503-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5503-128">CommonParameters</span></span>
<span data-ttu-id="c5503-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5503-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5503-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c5503-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5503-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="c5503-131">INPUTS</span></span>

### <span data-ttu-id="c5503-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c5503-132">System.String</span></span>

### <span data-ttu-id="c5503-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="c5503-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="c5503-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c5503-134">OUTPUTS</span></span>

### <span data-ttu-id="c5503-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="c5503-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="c5503-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="c5503-136">NOTES</span></span>

## <span data-ttu-id="c5503-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c5503-137">RELATED LINKS</span></span>
