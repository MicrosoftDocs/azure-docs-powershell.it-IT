---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: 8a85f3dff99184be984a7b08c7a4cafe25c697d1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678740"
---
# <span data-ttu-id="2b6eb-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="2b6eb-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="2b6eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b6eb-102">SYNOPSIS</span></span>
<span data-ttu-id="2b6eb-103">Ottiene i dettagli di un pool di file di Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="2b6eb-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="2b6eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b6eb-104">SYNTAX</span></span>

### <span data-ttu-id="2b6eb-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2b6eb-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b6eb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b6eb-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b6eb-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b6eb-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b6eb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b6eb-108">DESCRIPTION</span></span>
<span data-ttu-id="2b6eb-109">Il cmdlet **Get-AzNetAppFilesPool** ottiene i dettagli di un pool di ANF.</span><span class="sxs-lookup"><span data-stu-id="2b6eb-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="2b6eb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b6eb-110">EXAMPLES</span></span>

### <span data-ttu-id="2b6eb-111">Esempio 1: ottenere un pool di ANF</span><span class="sxs-lookup"><span data-stu-id="2b6eb-111">Example 1: Get an ANF pool</span></span>
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

<span data-ttu-id="2b6eb-112">Questo comando consente di ottenere l'account denominato MyAnfPool dall'account "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="2b6eb-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="2b6eb-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b6eb-113">PARAMETERS</span></span>

### <span data-ttu-id="2b6eb-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2b6eb-114">-AccountName</span></span>
<span data-ttu-id="2b6eb-115">Nome dell'account di ANF</span><span class="sxs-lookup"><span data-stu-id="2b6eb-115">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6eb-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="2b6eb-116">-AccountObject</span></span>
<span data-ttu-id="2b6eb-117">Oggetto account che contiene il pool da restituire</span><span class="sxs-lookup"><span data-stu-id="2b6eb-117">The account object containing the pool to return</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b6eb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b6eb-118">-DefaultProfile</span></span>
<span data-ttu-id="2b6eb-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b6eb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6eb-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="2b6eb-120">-Name</span></span>
<span data-ttu-id="2b6eb-121">Nome del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="2b6eb-121">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: PoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6eb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b6eb-122">-ResourceGroupName</span></span>
<span data-ttu-id="2b6eb-123">Gruppo risorse del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="2b6eb-123">The resource group of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b6eb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b6eb-124">-ResourceId</span></span>
<span data-ttu-id="2b6eb-125">ID risorsa del pool di ANF</span><span class="sxs-lookup"><span data-stu-id="2b6eb-125">The resource id of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b6eb-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b6eb-126">CommonParameters</span></span>
<span data-ttu-id="2b6eb-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b6eb-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2b6eb-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b6eb-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b6eb-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b6eb-129">INPUTS</span></span>

### <span data-ttu-id="2b6eb-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2b6eb-130">System.String</span></span>

### <span data-ttu-id="2b6eb-131">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="2b6eb-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="2b6eb-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b6eb-132">OUTPUTS</span></span>

### <span data-ttu-id="2b6eb-133">Microsoft. Azure. Commands. NetAppFiles. Models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="2b6eb-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="2b6eb-134">Note</span><span class="sxs-lookup"><span data-stu-id="2b6eb-134">NOTES</span></span>

## <span data-ttu-id="2b6eb-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b6eb-135">RELATED LINKS</span></span>
