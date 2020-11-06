---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 015E3BC9-C535-4EA2-8A30-C728385DBFF8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
ms.openlocfilehash: 77c2df1ec61b42aaded458bea564cf6c953c90ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519916"
---
# <span data-ttu-id="52573-101">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="52573-101">New-AzureRmBackupVault</span></span>

## <span data-ttu-id="52573-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="52573-102">SYNOPSIS</span></span>
<span data-ttu-id="52573-103">Crea un caveau di backup.</span><span class="sxs-lookup"><span data-stu-id="52573-103">Creates a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52573-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52573-104">SYNTAX</span></span>

```
New-AzureRmBackupVault [-ResourceGroupName] <String> [-Name] <String> [-Region] <String>
 [[-Storage] <AzureBackupVaultStorageType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52573-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="52573-105">DESCRIPTION</span></span>
<span data-ttu-id="52573-106">Il cmdlet **New-AzureRmBackupVault** crea un Vault di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="52573-106">The **New-AzureRmBackupVault** cmdlet creates an Azure Backup vault.</span></span>
<span data-ttu-id="52573-107">Questo cmdlet restituisce un oggetto **AzureRmBackupVault** che funge da riferimento all'entità Vault.</span><span class="sxs-lookup"><span data-stu-id="52573-107">This cmdlet returns an **AzureRmBackupVault** object that acts as a reference to the vault entity.</span></span>

## <span data-ttu-id="52573-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52573-108">EXAMPLES</span></span>

### <span data-ttu-id="52573-109">Esempio 1: creare un Vault di backup</span><span class="sxs-lookup"><span data-stu-id="52573-109">Example 1: Create a backup vault</span></span>
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup01" -Name "Vault03" -Region "westus"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup01/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="52573-110">Questo comando crea un Vault di backup di Azure denominato Vault03.</span><span class="sxs-lookup"><span data-stu-id="52573-110">This command creates an Azure Backup vault named Vault03.</span></span>
<span data-ttu-id="52573-111">Il Vault si trova nel gruppo risorse denominato ResourceGroup01 nell'area ovest degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="52573-111">The vault is in the resource group named ResourceGroup01 in the West US region.</span></span>
<span data-ttu-id="52573-112">Il Vault usa il tipo di archiviazione georidondante predefinito.</span><span class="sxs-lookup"><span data-stu-id="52573-112">The vault uses the default GeoRedundant storage type.</span></span>

### <span data-ttu-id="52573-113">Esempio 2: creare un archivio di backup che usa lo spazio di archiviazione locale ridondante</span><span class="sxs-lookup"><span data-stu-id="52573-113">Example 2: Create a backup vault that uses locally redundant storage</span></span>
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup02" -Name "Vault03" -Region "westus" -Storage LocallyRedundant
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup02/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup02
Region            : westus
Storage           : LocallyRedundant
```

<span data-ttu-id="52573-114">Questo comando crea un Vault di backup di Azure denominato Vault03.</span><span class="sxs-lookup"><span data-stu-id="52573-114">This command creates an Azure Backup vault named Vault03.</span></span>
<span data-ttu-id="52573-115">Il Vault si trova nel gruppo risorse denominato ResourceGroup02 nell'area ovest degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="52573-115">The vault is in the resource group named ResourceGroup02 in the West US region.</span></span>
<span data-ttu-id="52573-116">Il Vault usa il tipo di archiviazione LocallyRedundant.</span><span class="sxs-lookup"><span data-stu-id="52573-116">The vault uses the LocallyRedundant storage type.</span></span>

## <span data-ttu-id="52573-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="52573-117">PARAMETERS</span></span>

### <span data-ttu-id="52573-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52573-118">-DefaultProfile</span></span>
<span data-ttu-id="52573-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="52573-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52573-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="52573-120">-Name</span></span>
<span data-ttu-id="52573-121">Specifica un nome per l'archiviazione di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="52573-121">Specifies a name for the Azure Backup vault.</span></span>
<span data-ttu-id="52573-122">Il nome deve essere univoco in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="52573-122">The name must be unique in a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52573-123">-Area geografica</span><span class="sxs-lookup"><span data-stu-id="52573-123">-Region</span></span>
<span data-ttu-id="52573-124">Specifica un'area di Azure in cui è presente il Vault di backup.</span><span class="sxs-lookup"><span data-stu-id="52573-124">Specifies an Azure region in which the backup vault exists.</span></span>
<span data-ttu-id="52573-125">Per gli scenari di backup ibridi, è consigliabile creare un Vault in un'area vicina al server locale per ridurre la latenza.</span><span class="sxs-lookup"><span data-stu-id="52573-125">For hybrid backup scenarios, we recommend that you create a vault in a region close to the on-premise server to reduce latency.</span></span>
<span data-ttu-id="52573-126">Per il backup delle macchine virtuali dell'infrastruttura Azure come servizio (IaaS), il Vault diventa il punto di individuazione per le macchine virtuali locali.</span><span class="sxs-lookup"><span data-stu-id="52573-126">For backup of Azure infrastructure as a service (IaaS) virtual machines, the vault becomes the point of discovery for local virtual machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52573-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52573-127">-ResourceGroupName</span></span>
<span data-ttu-id="52573-128">Specifica il nome di un gruppo di risorse Azure esistente in cui questo cmdlet crea un Vault di backup.</span><span class="sxs-lookup"><span data-stu-id="52573-128">Specifies the name of an existing Azure resource group in which this cmdlet creates a Backup vault.</span></span>
<span data-ttu-id="52573-129">Per creare un gruppo di risorse, usare il cmdlet New-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="52573-129">To create a resource group, use the New-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="52573-130">Il gruppo risorse e il Vault di backup di Azure non devono essere nella stessa area geografica.</span><span class="sxs-lookup"><span data-stu-id="52573-130">The resource group and the Azure Backup vault do not have to be in the same region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52573-131">-Spazio di archiviazione</span><span class="sxs-lookup"><span data-stu-id="52573-131">-Storage</span></span>
<span data-ttu-id="52573-132">Specifica il tipo di archiviazione per i dati di backup.</span><span class="sxs-lookup"><span data-stu-id="52573-132">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="52573-133">I valori accettabili per questo parametro sono: LocallyRedundant e georidondanti.</span><span class="sxs-lookup"><span data-stu-id="52573-133">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>
<span data-ttu-id="52573-134">Il valore predefinito è georidondante.</span><span class="sxs-lookup"><span data-stu-id="52573-134">The default value is GeoRedundant.</span></span>

```yaml
Type: AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52573-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52573-135">CommonParameters</span></span>
<span data-ttu-id="52573-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52573-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52573-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52573-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52573-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="52573-138">INPUTS</span></span>

### <span data-ttu-id="52573-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="52573-139">None</span></span>

## <span data-ttu-id="52573-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52573-140">OUTPUTS</span></span>

### <span data-ttu-id="52573-141">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="52573-141">AzureRmBackupVault</span></span>

## <span data-ttu-id="52573-142">Note</span><span class="sxs-lookup"><span data-stu-id="52573-142">NOTES</span></span>
* <span data-ttu-id="52573-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="52573-143">None</span></span>

## <span data-ttu-id="52573-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52573-144">RELATED LINKS</span></span>

[<span data-ttu-id="52573-145">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="52573-145">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="52573-146">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="52573-146">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="52573-147">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="52573-147">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


