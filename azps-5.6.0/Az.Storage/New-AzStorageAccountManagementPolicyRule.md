---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyRule.md
ms.openlocfilehash: 73606a2af9ff0c5e948d407dd5da1f21df5d14b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002621"
---
# <span data-ttu-id="c773c-101">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="c773c-101">New-AzStorageAccountManagementPolicyRule</span></span>

## <span data-ttu-id="c773c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c773c-102">SYNOPSIS</span></span>
<span data-ttu-id="c773c-103">Crea un oggetto regola ManagementPolicy, che può essere usato in Set-AzStorageAccountManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="c773c-103">Creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="c773c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c773c-104">SYNTAX</span></span>

```
New-AzStorageAccountManagementPolicyRule [-Name] <String> [-Disabled] -Action <PSManagementPolicyActionGroup>
 [-Filter <PSManagementPolicyRuleFilter>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c773c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c773c-105">DESCRIPTION</span></span>
<span data-ttu-id="c773c-106">Il cmdlet **New-AzStorageAccountManagementPolicyRule** crea un oggetto regola ManagementPolicy, che può essere usato in Set-AzStorageAccountManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="c773c-106">The **New-AzStorageAccountManagementPolicyRule** cmdlet creates a ManagementPolicy rule object, which can be used in Set-AzStorageAccountManagementPolicy.</span></span>

## <span data-ttu-id="c773c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c773c-107">EXAMPLES</span></span>

### <span data-ttu-id="c773c-108">Esempio 1: crea un oggetto regola ManagementPolicy, quindi impostato su un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c773c-108">Example 1: Creates a ManagementPolicy rule object, then set to a Storage Account</span></span>
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

<span data-ttu-id="c773c-109">Questo comando crea un oggetto regola ManagementPolicy, con un oggetto gruppo di azioni ManagementPolicy contiene 4 azioni, un oggetto filtro della regola ManagementPolicy, quindi imposta la regola su un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c773c-109">This command create a ManagementPolicy rule object, with a ManagementPolicy action group object contains 4 actions, a ManagementPolicy rule filter object, then set the rule to a Storage Account.</span></span>

## <span data-ttu-id="c773c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c773c-110">PARAMETERS</span></span>

### <span data-ttu-id="c773c-111">-Action</span><span class="sxs-lookup"><span data-stu-id="c773c-111">-Action</span></span>
<span data-ttu-id="c773c-112">Oggetto che definisce il set di azioni.</span><span class="sxs-lookup"><span data-stu-id="c773c-112">An object that defines the action set.</span></span>
<span data-ttu-id="c773c-113">Ottenere l'oggetto con i nomi dei cmdletAdd-AzureStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="c773c-113">Get the Object with cmdlet Add-AzureStorageAccountManagementPolicyAction</span></span>

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

### <span data-ttu-id="c773c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c773c-114">-DefaultProfile</span></span>
<span data-ttu-id="c773c-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c773c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c773c-116">-Disabled</span><span class="sxs-lookup"><span data-stu-id="c773c-116">-Disabled</span></span>
<span data-ttu-id="c773c-117">Se impostata, la regola viene disabilitata.</span><span class="sxs-lookup"><span data-stu-id="c773c-117">The rule is disabled if set it.</span></span>

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

### <span data-ttu-id="c773c-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="c773c-118">-Filter</span></span>
<span data-ttu-id="c773c-119">Oggetto che definisce il set di filtri.</span><span class="sxs-lookup"><span data-stu-id="c773c-119">An object that defines the filter set.</span></span>
<span data-ttu-id="c773c-120">Ottenere l'oggetto con i nomi dei cmdletNew-AzureStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="c773c-120">Get the Object with cmdlet New-AzureStorageAccountManagementPolicyFilter</span></span>

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

### <span data-ttu-id="c773c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c773c-121">-Name</span></span>
<span data-ttu-id="c773c-122">Il nome di una regola può contenere qualsiasi combinazione di caratteri alfanumerici.</span><span class="sxs-lookup"><span data-stu-id="c773c-122">A rule name can contain any combination of alpha numeric characters.</span></span>
<span data-ttu-id="c773c-123">Per il nome della regola viene applicata la distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="c773c-123">Rule name is case-sensitive.</span></span>
<span data-ttu-id="c773c-124">Deve essere univoco all'interno di un criterio.</span><span class="sxs-lookup"><span data-stu-id="c773c-124">It must be unique within a policy.</span></span>

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

### <span data-ttu-id="c773c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c773c-125">CommonParameters</span></span>
<span data-ttu-id="c773c-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c773c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c773c-127">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c773c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c773c-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="c773c-128">INPUTS</span></span>

### <span data-ttu-id="c773c-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c773c-129">None</span></span>

## <span data-ttu-id="c773c-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c773c-130">OUTPUTS</span></span>

### <span data-ttu-id="c773c-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="c773c-131">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule</span></span>

## <span data-ttu-id="c773c-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="c773c-132">NOTES</span></span>

## <span data-ttu-id="c773c-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c773c-133">RELATED LINKS</span></span>
