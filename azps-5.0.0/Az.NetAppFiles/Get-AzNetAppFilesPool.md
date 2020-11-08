---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: 257421a43c3da11c82316eaf58d2983fe47d5f05
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201075"
---
# <span data-ttu-id="4641e-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="4641e-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="4641e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4641e-102">SYNOPSIS</span></span>
<span data-ttu-id="4641e-103">Ottiene i dettagli di un pool di file di Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="4641e-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="4641e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4641e-104">SYNTAX</span></span>

### <span data-ttu-id="4641e-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4641e-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4641e-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4641e-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4641e-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4641e-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4641e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4641e-108">DESCRIPTION</span></span>
<span data-ttu-id="4641e-109">Il cmdlet **Get-AzNetAppFilesPool** ottiene i dettagli di un pool di ANF.</span><span class="sxs-lookup"><span data-stu-id="4641e-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="4641e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4641e-110">EXAMPLES</span></span>

### <span data-ttu-id="4641e-111">Esempio 1: ottenere un pool di ANF</span><span class="sxs-lookup"><span data-stu-id="4641e-111">Example 1: Get an ANF pool</span></span>
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
ProvisioningState : Succeeded
```

<span data-ttu-id="4641e-112">Questo comando consente di ottenere l'account denominato MyAnfPool dall'account "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="4641e-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="4641e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4641e-113">PARAMETERS</span></span>

### <span data-ttu-id="4641e-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4641e-114">-AccountName</span></span>
<span data-ttu-id="4641e-115">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="4641e-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="4641e-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="4641e-116">-AccountObject</span></span>
<span data-ttu-id="4641e-117">Oggetto account che contiene il pool da restituire</span><span class="sxs-lookup"><span data-stu-id="4641e-117">The account object containing the pool to return</span></span>

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

### <span data-ttu-id="4641e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4641e-118">-DefaultProfile</span></span>
<span data-ttu-id="4641e-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4641e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4641e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="4641e-120">-Name</span></span>
<span data-ttu-id="4641e-121">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="4641e-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="4641e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4641e-122">-ResourceGroupName</span></span>
<span data-ttu-id="4641e-123">Gruppo risorse del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="4641e-123">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="4641e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4641e-124">-ResourceId</span></span>
<span data-ttu-id="4641e-125">ID risorsa del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="4641e-125">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="4641e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4641e-126">CommonParameters</span></span>
<span data-ttu-id="4641e-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4641e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4641e-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4641e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4641e-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4641e-129">INPUTS</span></span>

### <span data-ttu-id="4641e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4641e-130">System.String</span></span>

### <span data-ttu-id="4641e-131">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="4641e-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="4641e-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4641e-132">OUTPUTS</span></span>

### <span data-ttu-id="4641e-133">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="4641e-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="4641e-134">Note</span><span class="sxs-lookup"><span data-stu-id="4641e-134">NOTES</span></span>

## <span data-ttu-id="4641e-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4641e-135">RELATED LINKS</span></span>
