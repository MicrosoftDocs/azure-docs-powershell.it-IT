---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/Az.storage/set-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: cc91184374575b25f34669d7e22c80b620d34ced
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976173"
---
# <span data-ttu-id="88b56-101">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="88b56-101">Set-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="88b56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88b56-102">SYNOPSIS</span></span>
<span data-ttu-id="88b56-103">Crea o modifica i criteri di gestione di un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="88b56-103">Creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="88b56-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88b56-104">SYNTAX</span></span>

### <span data-ttu-id="88b56-105">AccountNamePolicyRule (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="88b56-105">AccountNamePolicyRule (Default)</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Rule <PSManagementPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88b56-106">AccountNamePolicyObject</span><span class="sxs-lookup"><span data-stu-id="88b56-106">AccountNamePolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Policy <PSManagementPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="88b56-107">AccountObjectPolicyRule</span><span class="sxs-lookup"><span data-stu-id="88b56-107">AccountObjectPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88b56-108">AccountObjectPolicyObject</span><span class="sxs-lookup"><span data-stu-id="88b56-108">AccountObjectPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88b56-109">AccountResourceIdPolicyRule</span><span class="sxs-lookup"><span data-stu-id="88b56-109">AccountResourceIdPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88b56-110">AccountResourceIdPolicyObject</span><span class="sxs-lookup"><span data-stu-id="88b56-110">AccountResourceIdPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88b56-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="88b56-111">DESCRIPTION</span></span>
<span data-ttu-id="88b56-112">Il cmdlet **Set-AzStorageAccountManagementPolicy** crea o modifica il criterio di gestione di un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="88b56-112">The **Set-AzStorageAccountManagementPolicy** cmdlet creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="88b56-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88b56-113">EXAMPLES</span></span>

### <span data-ttu-id="88b56-114">Esempio 1: Creare o aggiornare il criterio di gestione di un account di archiviazione con oggetti regola ManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="88b56-114">Example 1: Create or update the management policy of a Storage account with ManagementPolicy rule objects.</span></span>
```
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -SnapshotAction Delete -daysAfterCreationGreaterThan 100
PS C:\>$filter1 = New-AzStorageAccountManagementPolicyFilter -PrefixMatch ab,cd 
PS C:\>$rule1 = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action1 -Filter $filter1

PS C:\>$action2 = Add-AzStorageAccountManagementPolicyAction -SnapshotAction Delete -daysAfterCreationGreaterThan 100
PS C:\>$action2 = Add-AzStorageAccountManagementPolicyAction -InputObject $action2 -BlobVersionAction Delete -daysAfterCreationGreaterThan 100
PS C:\>$filter2 = New-AzStorageAccountManagementPolicyFilter -BlobType appendBlob,blockBlob
PS C:\>$rule2 = New-AzStorageAccountManagementPolicyRule -Name Test2 -Action $action2 -Filter $filter2

PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule1,$rule2


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 2/19/2021 10:13:00 AM
Rules              : [
                         {
                             "Enabled":  true,
                             "Name":  "Test",
                             "Definition":  {
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
                                                                                            },
                                                                                 "TierToCool":  null,
                                                                                 "TierToArchive":  null
                                                                             },
                                                                "Version":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  [
                                                                                    "ab",
                                                                                    "cd"
                                                                                ],
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         },
                         {
                             "Enabled":  true,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  null,
                                                                "Snapshot":  {
                                                                                 "Delete":  {
                                                                                                "DaysAfterCreationGreaterThan":  100
                                                                                            },
                                                                                 "TierToCool":  null,
                                                                                 "TierToArchive":  null
                                                                             },
                                                                "Version":  {
                                                                                "Delete":  {
                                                                                               "DaysAfterCreationGreaterThan":  100
                                                                                           },
                                                                                "TierToCool":  null,
                                                                                "TierToArchive":  null
                                                                            }
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "appendBlob",
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="88b56-115">Questo comando crea prima di tutto 2 oggetti regola ManagementPolicy, quindi crea o aggiorna il criterio di gestione di un account di archiviazione con gli oggetti regola 2 ManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="88b56-115">This command first create 2 ManagementPolicy rule objects, then creates or updates the management policy of a Storage account with the 2 ManagementPolicy rule objects.</span></span>

### <span data-ttu-id="88b56-116">Esempio 2: Creare o aggiornare i criteri di gestione di un account di archiviazione con criteri in formato Json.</span><span class="sxs-lookup"><span data-stu-id="88b56-116">Example 2: Create or update the management policy of a Storage account with a Json format policy.</span></span>
```
PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Policy (@{
    Rules=(@{
        Enabled=$true;
        Name="Test";
        Definition=(@{
            Actions=(@{
                BaseBlob=(@{
                    TierToCool=@{DaysAfterModificationGreaterThan=30};
                    TierToArchive=@{DaysAfterModificationGreaterThan=50};
                    Delete=@{DaysAfterModificationGreaterThan=100};
                });
                Snapshot=(@{
                    Delete=@{DaysAfterCreationGreaterThan=100};
                    TierToArchive=@{DaysAfterCreationGreaterThan=50};
                    TierToCool=@{DaysAfterCreationGreaterThan=60};
                });
                Version=(@{
                    Delete=@{DaysAfterCreationGreaterThan=100};
                    TierToArchive=@{DaysAfterCreationGreaterThan=50};
                    TierToCool=@{DaysAfterCreationGreaterThan=60};
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob");
                PrefixMatch=@("prefix1","prefix2");
            })
        })
    },
    @{
        Enabled=$false;
        Name="Test2";
        Definition=(@{
            Actions=(@{
                Version=(@{
                    Delete=@{DaysAfterCreationGreaterThan=100};
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob","appendBlob");
            })
        })
    })
})


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 2/19/2021 10:16:32 AM
Rules              : [
                         {
                             "Enabled":  true,
                             "Name":  "Test",
                             "Definition":  {
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
                                                                                            },
                                                                                 "TierToCool":  {
                                                                                                    "DaysAfterCreationGreaterThan":  60
                                                                                                },
                                                                                 "TierToArchive":  {
                                                                                                       "DaysAfterCreationGreaterThan":  50
                                                                                                   }
                                                                             },
                                                                "Version":  {
                                                                                "Delete":  {
                                                                                               "DaysAfterCreationGreaterThan":  100
                                                                                           },
                                                                                "TierToCool":  {
                                                                                                   "DaysAfterCreationGreaterThan":  60
                                                                                               },
                                                                                "TierToArchive":  {
                                                                                                      "DaysAfterCreationGreaterThan":  50
                                                                                                  }
                                                                            }
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  [
                                                                                    "prefix1",
                                                                                    "prefix2"
                                                                                ],
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         },
                         {
                             "Enabled":  false,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  null,
                                                                "Snapshot":  null,
                                                                "Version":  {
                                                                                "Delete":  {
                                                                                               "DaysAfterCreationGreaterThan":  100
                                                                                           },
                                                                                "TierToCool":  null,
                                                                                "TierToArchive":  null
                                                                            }
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob",
                                                                                  "appendBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="88b56-117">Questo comando crea o aggiorna i criteri di gestione di un account di archiviazione con criteri in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="88b56-117">This command creates or updates the management policy of a Storage account with a json format policy.</span></span>

### <span data-ttu-id="88b56-118">Esempio 3: Ottenere i criteri di gestione da un account di archiviazione, quindi impostarlo su un altro account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="88b56-118">Example 3: Get the management policy from a Storage account, then set it to another Storage account.</span></span>
```
PS C:\>$outputPolicy = Get-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" | Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup2" -AccountName "mystorageaccount2"
```

<span data-ttu-id="88b56-119">Questo comando recupera prima i criteri di gestione da un account di archiviazione, quindi lo imposta su un altro account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="88b56-119">This command first gets the management policy from a Storage account, then set it to another Storage account.</span></span>

## <span data-ttu-id="88b56-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88b56-120">PARAMETERS</span></span>

### <span data-ttu-id="88b56-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b56-121">-DefaultProfile</span></span>
<span data-ttu-id="88b56-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="88b56-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88b56-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="88b56-123">-Policy</span></span>
<span data-ttu-id="88b56-124">Oggetto Criteri di gestione da impostare</span><span class="sxs-lookup"><span data-stu-id="88b56-124">Management Policy Object to Set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy
Parameter Sets: AccountNamePolicyObject, AccountObjectPolicyObject, AccountResourceIdPolicyObject
Aliases: ManagementPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88b56-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88b56-125">-ResourceGroupName</span></span>
<span data-ttu-id="88b56-126">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="88b56-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNamePolicyRule, AccountNamePolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b56-127">-Rule</span><span class="sxs-lookup"><span data-stu-id="88b56-127">-Rule</span></span>
<span data-ttu-id="88b56-128">Regole dei criteri di gestione.</span><span class="sxs-lookup"><span data-stu-id="88b56-128">The Management Policy rules.</span></span> <span data-ttu-id="88b56-129">Ottenere l'oggetto con New-AzStorageAccountManagementPolicyRule cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88b56-129">Get the object with New-AzStorageAccountManagementPolicyRule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicyRule[]
Parameter Sets: AccountNamePolicyRule, AccountObjectPolicyRule, AccountResourceIdPolicyRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88b56-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="88b56-130">-StorageAccount</span></span>
<span data-ttu-id="88b56-131">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="88b56-131">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObjectPolicyRule, AccountObjectPolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88b56-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="88b56-132">-StorageAccountName</span></span>
<span data-ttu-id="88b56-133">Nome account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="88b56-133">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNamePolicyRule, AccountNamePolicyObject
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b56-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="88b56-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="88b56-135">ID risorsa account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="88b56-135">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceIdPolicyRule, AccountResourceIdPolicyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88b56-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88b56-136">-Confirm</span></span>
<span data-ttu-id="88b56-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88b56-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b56-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88b56-138">-WhatIf</span></span>
<span data-ttu-id="88b56-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88b56-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88b56-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88b56-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b56-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b56-141">CommonParameters</span></span>
<span data-ttu-id="88b56-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88b56-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b56-143">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88b56-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b56-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="88b56-144">INPUTS</span></span>

### <span data-ttu-id="88b56-145">System.String</span><span class="sxs-lookup"><span data-stu-id="88b56-145">System.String</span></span>

## <span data-ttu-id="88b56-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88b56-146">OUTPUTS</span></span>

### <span data-ttu-id="88b56-147">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="88b56-147">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy</span></span>

## <span data-ttu-id="88b56-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="88b56-148">NOTES</span></span>

## <span data-ttu-id="88b56-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88b56-149">RELATED LINKS</span></span>
