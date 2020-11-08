---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesreplicationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
ms.openlocfilehash: a2345dfe37fd43532739cdfd8000b47fb1e20906
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201072"
---
# <span data-ttu-id="b64b5-101">Get-AzNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="b64b5-101">Get-AzNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="b64b5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b64b5-102">SYNOPSIS</span></span>
<span data-ttu-id="b64b5-103">Ottenere lo stato della replica</span><span class="sxs-lookup"><span data-stu-id="b64b5-103">Get the status of the replication</span></span>

## <span data-ttu-id="b64b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b64b5-104">SYNTAX</span></span>

### <span data-ttu-id="b64b5-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b64b5-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b64b5-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b64b5-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b64b5-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b64b5-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b64b5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b64b5-108">DESCRIPTION</span></span>
<span data-ttu-id="b64b5-109">Ottenere lo stato della replica</span><span class="sxs-lookup"><span data-stu-id="b64b5-109">Get the status of the replication</span></span>

## <span data-ttu-id="b64b5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b64b5-110">EXAMPLES</span></span>

### <span data-ttu-id="b64b5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b64b5-111">Example 1</span></span>
```powershell
PS C:\> Get-AnfReplicationStatus -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolName "MyDestinationPool" -VolumeName "MyVol"

Output:

Healthy            : true
RelationshipStatus : Idle
MirrorState        : Mirrored
TotalProgress      : 1024
ErrorMessage       :
```

<span data-ttu-id="b64b5-112">Questo comando ottiene lo stato della replica in MyVol</span><span class="sxs-lookup"><span data-stu-id="b64b5-112">This command gets the status of replication on MyVol</span></span>

## <span data-ttu-id="b64b5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b64b5-113">PARAMETERS</span></span>

### <span data-ttu-id="b64b5-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b64b5-114">-AccountName</span></span>
<span data-ttu-id="b64b5-115">Nome dell'account di ANF del volume di destinazione della replica</span><span class="sxs-lookup"><span data-stu-id="b64b5-115">The name of the ANF account of the replication destination volume</span></span>

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

### <span data-ttu-id="b64b5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b64b5-116">-DefaultProfile</span></span>
<span data-ttu-id="b64b5-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b64b5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b64b5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b64b5-118">-InputObject</span></span>
<span data-ttu-id="b64b5-119">Oggetto volume di destinazione della replica ANF per ottenere lo stato di replica</span><span class="sxs-lookup"><span data-stu-id="b64b5-119">The ANF replication destination volume object to get replication status</span></span>

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

### <span data-ttu-id="b64b5-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b64b5-120">-Name</span></span>
<span data-ttu-id="b64b5-121">Nome del volume di destinazione della replica di ANF</span><span class="sxs-lookup"><span data-stu-id="b64b5-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="b64b5-122">-PoolName</span><span class="sxs-lookup"><span data-stu-id="b64b5-122">-PoolName</span></span>
<span data-ttu-id="b64b5-123">Nome del pool di ANF del volume di destinazione della replica</span><span class="sxs-lookup"><span data-stu-id="b64b5-123">The name of the ANF pool of the replication destination volume</span></span>

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

### <span data-ttu-id="b64b5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b64b5-124">-ResourceGroupName</span></span>
<span data-ttu-id="b64b5-125">Gruppo risorse del volume di destinazione della replica di ANF</span><span class="sxs-lookup"><span data-stu-id="b64b5-125">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="b64b5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b64b5-126">-ResourceId</span></span>
<span data-ttu-id="b64b5-127">ID risorsa del volume di destinazione della replica di ANF</span><span class="sxs-lookup"><span data-stu-id="b64b5-127">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="b64b5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b64b5-128">CommonParameters</span></span>
<span data-ttu-id="b64b5-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b64b5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b64b5-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b64b5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b64b5-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b64b5-131">INPUTS</span></span>

### <span data-ttu-id="b64b5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b64b5-132">System.String</span></span>

## <span data-ttu-id="b64b5-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b64b5-133">OUTPUTS</span></span>

### <span data-ttu-id="b64b5-134">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="b64b5-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="b64b5-135">Note</span><span class="sxs-lookup"><span data-stu-id="b64b5-135">NOTES</span></span>

## <span data-ttu-id="b64b5-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b64b5-136">RELATED LINKS</span></span>
