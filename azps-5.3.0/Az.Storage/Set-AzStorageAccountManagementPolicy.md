---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/set-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: b52dc34ddffb2234962888407ed67c487f4195c4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474638"
---
# <span data-ttu-id="aa222-101">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="aa222-101">Set-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="aa222-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aa222-102">SYNOPSIS</span></span>
<span data-ttu-id="aa222-103">Crea o modifica i criteri di gestione di un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="aa222-103">Creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="aa222-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa222-104">SYNTAX</span></span>

### <span data-ttu-id="aa222-105">AccountNamePolicyRule (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aa222-105">AccountNamePolicyRule (Default)</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Rule <PSManagementPolicyRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa222-106">AccountNamePolicyObject</span><span class="sxs-lookup"><span data-stu-id="aa222-106">AccountNamePolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Policy <PSManagementPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa222-107">AccountObjectPolicyRule</span><span class="sxs-lookup"><span data-stu-id="aa222-107">AccountObjectPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa222-108">AccountObjectPolicyObject</span><span class="sxs-lookup"><span data-stu-id="aa222-108">AccountObjectPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa222-109">AccountResourceIdPolicyRule</span><span class="sxs-lookup"><span data-stu-id="aa222-109">AccountResourceIdPolicyRule</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Rule <PSManagementPolicyRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa222-110">AccountResourceIdPolicyObject</span><span class="sxs-lookup"><span data-stu-id="aa222-110">AccountResourceIdPolicyObject</span></span>
```
Set-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> -Policy <PSManagementPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa222-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa222-111">DESCRIPTION</span></span>
<span data-ttu-id="aa222-112">Il cmdlet **set-AzStorageAccountManagementPolicy** crea o modifica i criteri di gestione di un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="aa222-112">The **Set-AzStorageAccountManagementPolicy** cmdlet creates or modifies the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="aa222-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa222-113">EXAMPLES</span></span>

### <span data-ttu-id="aa222-114">Esempio 1: creare o aggiornare i criteri di gestione di un account di archiviazione con gli oggetti della regola ManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="aa222-114">Example 1: Create or update the management policy of a Storage account with ManagementPolicy rule objects.</span></span>
```
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToArchive -daysAfterModificationGreaterThan 50
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -BaseBlobAction TierToCool -daysAfterModificationGreaterThan 30
PS C:\>$action1 = Add-AzStorageAccountManagementPolicyAction -InputObject $action1 -SnapshotAction Delete -daysAfterCreationGreaterThan 100
PS C:\>$filter1 = New-AzStorageAccountManagementPolicyFilter -PrefixMatch ab,cd 
PS C:\>$rule1 = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action1 -Filter $filter1

PS C:\>$action2 = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$filter2 = New-AzStorageAccountManagementPolicyFilter
PS C:\>$rule2 = New-AzStorageAccountManagementPolicyRule -Name Test2 -Action $action2 -Filter $filter2

PS C:\>Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule1,$rule2


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 10:29:29 AM
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
                             "Enabled":  true,
                             "Name":  "Test2",
                             "Definition":  {
                                                "Actions":  {
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  null,
                                                                                 "TierToArchive":  null,
                                                                                 "Delete":  {
                                                                                                "DaysAfterModificationGreaterThan":  100
                                                                                            }
                                                                             },
                                                                "Snapshot":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="aa222-115">Questo comando crea prima di tutto 2 oggetti della regola ManagementPolicy, quindi crea o aggiorna i criteri di gestione di un account di archiviazione con i 2 oggetti della regola ManagementPolicy.</span><span class="sxs-lookup"><span data-stu-id="aa222-115">This command first create 2 ManagementPolicy rule objects, then creates or updates the management policy of a Storage account with the 2 ManagementPolicy rule objects.</span></span>

### <span data-ttu-id="aa222-116">Esempio 2: creare o aggiornare i criteri di gestione di un account di archiviazione con un criterio di formato JSON.</span><span class="sxs-lookup"><span data-stu-id="aa222-116">Example 2: Create or update the management policy of a Storage account with a Json format policy.</span></span>
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
                BaseBlob=(@{
                    TierToCool=@{DaysAfterModificationGreaterThan=80};
                });
            });
            Filters=(@{
                BlobTypes=@("blockBlob");
            })
        })
    })
})


ResourceGroupName  : myresourcegroup
StorageAccountName : mystorageaccount
Id                 : /subscriptions/{subscription-id}/resourceGroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount/managementPolicies/default
Type               : Microsoft.Storage/storageAccounts/managementPolicies
LastModifiedTime   : 3/12/2019 10:24:55 AM
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
                                                                "BaseBlob":  {
                                                                                 "TierToCool":  {
                                                                                                    "DaysAfterModificationGreaterThan":  80
                                                                                                },
                                                                                 "TierToArchive":  null,
                                                                                 "Delete":  null
                                                                             },
                                                                "Snapshot":  null
                                                            },
                                                "Filters":  {
                                                                "PrefixMatch":  null,
                                                                "BlobTypes":  [
                                                                                  "blockBlob"
                                                                              ]
                                                            }
                                            }
                         }
                     ]
```

<span data-ttu-id="aa222-117">Questo comando crea o aggiorna i criteri di gestione di un account di archiviazione con un criterio in formato JSON.</span><span class="sxs-lookup"><span data-stu-id="aa222-117">This command creates or updates the management policy of a Storage account with a json format policy.</span></span>

### <span data-ttu-id="aa222-118">Esempio 3: ottenere i criteri di gestione da un account di archiviazione e impostarlo su un altro account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="aa222-118">Example 3: Get the management policy from a Storage account, then set it to another Storage account.</span></span>
```
PS C:\>$outputPolicy = Get-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" | Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup2" -AccountName "mystorageaccount2"
```

<span data-ttu-id="aa222-119">Questo comando ottiene prima i criteri di gestione da un account di archiviazione, quindi lo imposta su un altro account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="aa222-119">This command first gets the management policy from a Storage account, then set it to another Storage account.</span></span>

## <span data-ttu-id="aa222-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aa222-120">PARAMETERS</span></span>

### <span data-ttu-id="aa222-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa222-121">-DefaultProfile</span></span>
<span data-ttu-id="aa222-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aa222-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa222-123">-Policy</span><span class="sxs-lookup"><span data-stu-id="aa222-123">-Policy</span></span>
<span data-ttu-id="aa222-124">Oggetto Criteri di gestione da impostare</span><span class="sxs-lookup"><span data-stu-id="aa222-124">Management Policy Object to Set</span></span>

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

### <span data-ttu-id="aa222-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa222-125">-ResourceGroupName</span></span>
<span data-ttu-id="aa222-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aa222-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="aa222-127">-Regola</span><span class="sxs-lookup"><span data-stu-id="aa222-127">-Rule</span></span>
<span data-ttu-id="aa222-128">Regole dei criteri di gestione.</span><span class="sxs-lookup"><span data-stu-id="aa222-128">The Management Policy rules.</span></span> <span data-ttu-id="aa222-129">Ottenere l'oggetto con il cmdlet New-AzStorageAccountManagementPolicyRule.</span><span class="sxs-lookup"><span data-stu-id="aa222-129">Get the object with New-AzStorageAccountManagementPolicyRule cmdlet.</span></span>

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

### <span data-ttu-id="aa222-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa222-130">-StorageAccount</span></span>
<span data-ttu-id="aa222-131">Oggetto account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="aa222-131">Storage account object</span></span>

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

### <span data-ttu-id="aa222-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="aa222-132">-StorageAccountName</span></span>
<span data-ttu-id="aa222-133">Nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="aa222-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="aa222-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="aa222-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="aa222-135">ID risorsa account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="aa222-135">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="aa222-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aa222-136">-Confirm</span></span>
<span data-ttu-id="aa222-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa222-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa222-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa222-138">-WhatIf</span></span>
<span data-ttu-id="aa222-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa222-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa222-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa222-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa222-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa222-141">CommonParameters</span></span>
<span data-ttu-id="aa222-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa222-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa222-143">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa222-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa222-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aa222-144">INPUTS</span></span>

### <span data-ttu-id="aa222-145">System. String</span><span class="sxs-lookup"><span data-stu-id="aa222-145">System.String</span></span>

## <span data-ttu-id="aa222-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa222-146">OUTPUTS</span></span>

### <span data-ttu-id="aa222-147">Microsoft. Azure. Commands. Management. storage. Models. PSManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="aa222-147">Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy</span></span>

## <span data-ttu-id="aa222-148">Note</span><span class="sxs-lookup"><span data-stu-id="aa222-148">NOTES</span></span>

## <span data-ttu-id="aa222-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa222-149">RELATED LINKS</span></span>
