---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: 546364e96f7beed16ae8786dc3aaacbf9a84454d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968621"
---
# <span data-ttu-id="eab52-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="eab52-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="eab52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eab52-102">SYNOPSIS</span></span>
<span data-ttu-id="eab52-103">Recupera i dettagli di un pool di file (ANF) di Azure NetApp.</span><span class="sxs-lookup"><span data-stu-id="eab52-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="eab52-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eab52-104">SYNTAX</span></span>

### <span data-ttu-id="eab52-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="eab52-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eab52-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eab52-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eab52-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eab52-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eab52-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="eab52-108">DESCRIPTION</span></span>
<span data-ttu-id="eab52-109">Il cmdlet **Get-AzNetAppFilesPool** ottiene i dettagli di un pool ANF.</span><span class="sxs-lookup"><span data-stu-id="eab52-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="eab52-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eab52-110">EXAMPLES</span></span>

### <span data-ttu-id="eab52-111">Esempio 1: Ottenere un pool ANF</span><span class="sxs-lookup"><span data-stu-id="eab52-111">Example 1: Get an ANF pool</span></span>
```
PS C:\>Get-AzAnfPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
TotalThroughputMibps: 262.144
UtilizedThroughputMibps: 164.221
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="eab52-112">Questo comando recupera l'account denominato MyAnfPool dall'account "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="eab52-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="eab52-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eab52-113">PARAMETERS</span></span>

### <span data-ttu-id="eab52-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eab52-114">-AccountName</span></span>
<span data-ttu-id="eab52-115">Nome dell'account ANF</span><span class="sxs-lookup"><span data-stu-id="eab52-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="eab52-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="eab52-116">-AccountObject</span></span>
<span data-ttu-id="eab52-117">Oggetto account contenente il pool da restituire</span><span class="sxs-lookup"><span data-stu-id="eab52-117">The account object containing the pool to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eab52-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eab52-118">-DefaultProfile</span></span>
<span data-ttu-id="eab52-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="eab52-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eab52-120">-Name</span><span class="sxs-lookup"><span data-stu-id="eab52-120">-Name</span></span>
<span data-ttu-id="eab52-121">Nome del pool ANF</span><span class="sxs-lookup"><span data-stu-id="eab52-121">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: PoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eab52-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eab52-122">-ResourceGroupName</span></span>
<span data-ttu-id="eab52-123">Gruppo di risorse del pool ANF</span><span class="sxs-lookup"><span data-stu-id="eab52-123">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="eab52-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eab52-124">-ResourceId</span></span>
<span data-ttu-id="eab52-125">ID risorsa del pool ANF</span><span class="sxs-lookup"><span data-stu-id="eab52-125">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="eab52-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eab52-126">CommonParameters</span></span>
<span data-ttu-id="eab52-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eab52-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eab52-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="eab52-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eab52-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="eab52-129">INPUTS</span></span>

### <span data-ttu-id="eab52-130">System.String</span><span class="sxs-lookup"><span data-stu-id="eab52-130">System.String</span></span>

### <span data-ttu-id="eab52-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="eab52-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="eab52-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eab52-132">OUTPUTS</span></span>

### <span data-ttu-id="eab52-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="eab52-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="eab52-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="eab52-134">NOTES</span></span>

## <span data-ttu-id="eab52-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eab52-135">RELATED LINKS</span></span>
