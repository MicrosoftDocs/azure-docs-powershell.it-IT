---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
ms.openlocfilehash: c2a20d19676cff15ff26792a81bfc09242c5e4c2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195750"
---
# <span data-ttu-id="228c2-101">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="228c2-101">New-AzStorageAccountManagementPolicyRule</span></span>

## <span data-ttu-id="228c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="228c2-102">SYNOPSIS</span></span>
<span data-ttu-id="228c2-103">Crea un oggetto regola ManagementPolicy, che può essere usato in Set-AzStorageAccountManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="228c2-103">Creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="228c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="228c2-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyRule [-Name] <String> [-Disabled] -Action <PSManagementPolicyActionGroup>
 [-Filter <PSManagementPolicyRuleFilter>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="228c2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="228c2-105">DESCRIPTION</span></span>
<span data-ttu-id="228c2-106">Il cmdlet **New-AzStorageAccountManagementPolicyRule** crea un oggetto regola ManagementPolicy, che può essere usato in Set-AzStorageAccountManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="228c2-106">The **New-AzStorageAccountManagementPolicyRule** cmdlet creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="228c2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="228c2-107">EXAMPLES</span></span>

### <span data-ttu-id="228c2-108">Esempio 1: crea un oggetto regola ManagementPolicy, quindi impostato su un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="228c2-108">Example 1: Creates a ManagementPolicy rule object, then set to a Storage Account</span></span>
```
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50  -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30 -InputObject $action
PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100 -InputObject $action

PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2

PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name rule1 -Action $action -Filter $filter
PS C:\>$rule

Enabled    : True
Name       : rule1
Definition : {
                 "Actions":  {
                                 "BaseBlob":  {
                                                  "TierToCool":  {
                                                                     "DaysAfterModificationGreaterThan":  30
                                                                 },
                                                  "TierToArchive":  {
                                                                        "DaysAfterModificationGreaterThan":  50
                                                                    },
                                                  "Delete":  {
                                                                 "DaysAfterModificationGreaterThan":  100
                                                             }
                                              },
                                 "Snapshot":  {
                                                  "Delete":  {
                                                                 "DaysAfterCreationGreaterThan":  100
                                                             }
                                              }
                             },
                 "Filters":  {
                                 "PrefixMatch":  [
                                                     "blobprefix1",
                                                     "blobprefix2"
                                                 ],
                                 "BlobTypes":  [
                                                   "blockBlob"
                                               ]
                             }
             }

PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

<span data-ttu-id="228c2-109">Questo comando crea un oggetto regola ManagementPolicy, con un oggetto gruppo di azioni ManagementPolicy contiene 4 azioni, un oggetto filtro della regola ManagementPolicy, quindi imposta la regola su un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="228c2-109">This command create a ManagementPolicy rule object, with a ManagementPolicy action group object contains 4 actions, a ManagementPolicy rule filter object, then set the rule to a Storage Account.</span></span>

## <span data-ttu-id="228c2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="228c2-110">PARAMETERS</span></span>

### <span data-ttu-id="228c2-111">-Action</span><span class="sxs-lookup"><span data-stu-id="228c2-111">-Action</span></span>
<span data-ttu-id="228c2-112">Oggetto che definisce il set di azioni.</span><span class="sxs-lookup"><span data-stu-id="228c2-112">An object that defines the action set.</span></span>
<span data-ttu-id="228c2-113">Ottenere l'oggetto con i nomi dei cmdletAdd-AzureStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="228c2-113">Get the Object with cmdlet Add-AzureStorageAccountManagementPolicyAction</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyActionGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="228c2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="228c2-114">-DefaultProfile</span></span>
<span data-ttu-id="228c2-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="228c2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="228c2-116">-Disabled</span><span class="sxs-lookup"><span data-stu-id="228c2-116">-Disabled</span></span>
<span data-ttu-id="228c2-117">Se impostata, la regola viene disabilitata.</span><span class="sxs-lookup"><span data-stu-id="228c2-117">The rule is disabled if set it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="228c2-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="228c2-118">-Filter</span></span>
<span data-ttu-id="228c2-119">Oggetto che definisce il set di filtri.</span><span class="sxs-lookup"><span data-stu-id="228c2-119">An object that defines the filter set.</span></span>
<span data-ttu-id="228c2-120">Ottenere l'oggetto con i nomi dei cmdletNew-AzureStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="228c2-120">Get the Object with cmdlet New-AzureStorageAccountManagementPolicyFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRuleFilter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="228c2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="228c2-121">-Name</span></span>
<span data-ttu-id="228c2-122">Il nome di una regola può contenere qualsiasi combinazione di caratteri alfanumerici.</span><span class="sxs-lookup"><span data-stu-id="228c2-122">A rule name can contain any combination of alpha numeric characters.</span></span>
<span data-ttu-id="228c2-123">Per il nome della regola viene applicata la distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="228c2-123">Rule name is case-sensitive.</span></span>
<span data-ttu-id="228c2-124">Deve essere univoco all'interno di un criterio.</span><span class="sxs-lookup"><span data-stu-id="228c2-124">It must be unique within a policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="228c2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="228c2-125">CommonParameters</span></span>
<span data-ttu-id="228c2-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="228c2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="228c2-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="228c2-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="228c2-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="228c2-128">INPUTS</span></span>

### <span data-ttu-id="228c2-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="228c2-129">None</span></span>

## <span data-ttu-id="228c2-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="228c2-130">OUTPUTS</span></span>

### <span data-ttu-id="228c2-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="228c2-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span></span>

## <span data-ttu-id="228c2-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="228c2-132">NOTES</span></span>

## <span data-ttu-id="228c2-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="228c2-133">RELATED LINKS</span></span>
