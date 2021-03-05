---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesVolume.md
ms.openlocfilehash: 834a7444cda059614a7aa8b96acf99ba9cacd336
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968510"
---
# <span data-ttu-id="1a1be-101">Get-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="1a1be-101">Get-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="1a1be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a1be-102">SYNOPSIS</span></span>
<span data-ttu-id="1a1be-103">Recupera i dettagli di un volume FILE (ANF) di Azure NetApp.</span><span class="sxs-lookup"><span data-stu-id="1a1be-103">Gets details of an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="1a1be-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a1be-104">SYNTAX</span></span>

### <span data-ttu-id="1a1be-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1a1be-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a1be-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a1be-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesVolume -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a1be-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a1be-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesVolume -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a1be-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1a1be-108">DESCRIPTION</span></span>
<span data-ttu-id="1a1be-109">Il cmdlet **Get-AzNetAppFilesVolume** ottiene i dettagli di un volume ANF.</span><span class="sxs-lookup"><span data-stu-id="1a1be-109">The **Get-AzNetAppFilesVolume** cmdlet gets details of an ANF volume.</span></span>

## <span data-ttu-id="1a1be-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a1be-110">EXAMPLES</span></span>

### <span data-ttu-id="1a1be-111">Esempio 1: Ottenere un volume ANF</span><span class="sxs-lookup"><span data-stu-id="1a1be-111">Example 1: Get an ANF volume</span></span>
```
PS C:\>Get-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"

Output:

ResourceGroupName : MyRG
Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     :
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="1a1be-112">Questo comando recupera il volume denominato MyAnfVolume dal pool "MyAnfPool".</span><span class="sxs-lookup"><span data-stu-id="1a1be-112">This command gets the volume named MyAnfVolume from the pool "MyAnfPool".</span></span> 

## <span data-ttu-id="1a1be-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a1be-113">PARAMETERS</span></span>

### <span data-ttu-id="1a1be-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="1a1be-114">-AccountName</span></span>
<span data-ttu-id="1a1be-115">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="1a1be-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="1a1be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a1be-116">-DefaultProfile</span></span>
<span data-ttu-id="1a1be-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a1be-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a1be-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1a1be-118">-Name</span></span>
<span data-ttu-id="1a1be-119">Nome del volume ANF</span><span class="sxs-lookup"><span data-stu-id="1a1be-119">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a1be-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="1a1be-120">-PoolName</span></span>
<span data-ttu-id="1a1be-121">Nome del pool ANF</span><span class="sxs-lookup"><span data-stu-id="1a1be-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="1a1be-122">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="1a1be-122">-PoolObject</span></span>
<span data-ttu-id="1a1be-123">Oggetto pool contenente il volume da restituire</span><span class="sxs-lookup"><span data-stu-id="1a1be-123">The pool object containing the volume to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a1be-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a1be-124">-ResourceGroupName</span></span>
<span data-ttu-id="1a1be-125">Gruppo di risorse del volume ANF</span><span class="sxs-lookup"><span data-stu-id="1a1be-125">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="1a1be-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a1be-126">-ResourceId</span></span>
<span data-ttu-id="1a1be-127">ID risorsa del volume ANF</span><span class="sxs-lookup"><span data-stu-id="1a1be-127">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="1a1be-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a1be-128">CommonParameters</span></span>
<span data-ttu-id="1a1be-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a1be-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a1be-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1a1be-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a1be-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="1a1be-131">INPUTS</span></span>

### <span data-ttu-id="1a1be-132">System.String</span><span class="sxs-lookup"><span data-stu-id="1a1be-132">System.String</span></span>

### <span data-ttu-id="1a1be-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="1a1be-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="1a1be-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a1be-134">OUTPUTS</span></span>

### <span data-ttu-id="1a1be-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="1a1be-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="1a1be-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="1a1be-136">NOTES</span></span>

## <span data-ttu-id="1a1be-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a1be-137">RELATED LINKS</span></span>
