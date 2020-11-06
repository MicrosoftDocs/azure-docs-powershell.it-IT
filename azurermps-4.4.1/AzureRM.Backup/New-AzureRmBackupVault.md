---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 015E3BC9-C535-4EA2-8A30-C728385DBFF8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupVault.md
ms.openlocfilehash: a6415d941646f335ba7cae4fc2aab39d75000ab0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517080"
---
# <span data-ttu-id="50daa-101">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="50daa-101">New-AzureRmBackupVault</span></span>

## <span data-ttu-id="50daa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50daa-102">SYNOPSIS</span></span>
<span data-ttu-id="50daa-103">Crea un caveau di backup.</span><span class="sxs-lookup"><span data-stu-id="50daa-103">Creates a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50daa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50daa-104">SYNTAX</span></span>

```
New-AzureRmBackupVault [-ResourceGroupName] <String> [-Name] <String> [-Region] <String>
 [[-Storage] <AzureBackupVaultStorageType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50daa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50daa-105">DESCRIPTION</span></span>
<span data-ttu-id="50daa-106">Il cmdlet **New-AzureRmBackupVault** crea un Vault di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="50daa-106">The **New-AzureRmBackupVault** cmdlet creates an Azure Backup vault.</span></span>
<span data-ttu-id="50daa-107">Questo cmdlet restituisce un oggetto **AzureRmBackupVault** che funge da riferimento all'entità Vault.</span><span class="sxs-lookup"><span data-stu-id="50daa-107">This cmdlet returns an **AzureRmBackupVault** object that acts as a reference to the vault entity.</span></span>

## <span data-ttu-id="50daa-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50daa-108">EXAMPLES</span></span>

### <span data-ttu-id="50daa-109">Esempio 1: creare un Vault di backup</span><span class="sxs-lookup"><span data-stu-id="50daa-109">Example 1: Create a backup vault</span></span>
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup01" -Name "Vault03" -Region "westus"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup01/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="50daa-110">Questo comando crea un Vault di backup di Azure denominato Vault03.</span><span class="sxs-lookup"><span data-stu-id="50daa-110">This command creates an Azure Backup vault named Vault03.</span></span>
<span data-ttu-id="50daa-111">Il Vault si trova nel gruppo risorse denominato ResourceGroup01 nell'area ovest degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="50daa-111">The vault is in the resource group named ResourceGroup01 in the West US region.</span></span>
<span data-ttu-id="50daa-112">Il Vault usa il tipo di archiviazione georidondante predefinito.</span><span class="sxs-lookup"><span data-stu-id="50daa-112">The vault uses the default GeoRedundant storage type.</span></span>

### <span data-ttu-id="50daa-113">Esempio 2: creare un archivio di backup che usa lo spazio di archiviazione locale ridondante</span><span class="sxs-lookup"><span data-stu-id="50daa-113">Example 2: Create a backup vault that uses locally redundant storage</span></span>
```
PS C:\>New-AzureRmBackupVault -ResourceGroupName "ResourceGroup02" -Name "Vault03" -Region "westus" -Storage LocallyRedundant
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup02/providers/Microsoft.Backup
                    /BackupVault/Vault03
Name              : Vault03
ResourceGroupName : ResourceGroup02
Region            : westus
Storage           : LocallyRedundant
```

<span data-ttu-id="50daa-114">Questo comando crea un Vault di backup di Azure denominato Vault03.</span><span class="sxs-lookup"><span data-stu-id="50daa-114">This command creates an Azure Backup vault named Vault03.</span></span>
<span data-ttu-id="50daa-115">Il Vault si trova nel gruppo risorse denominato ResourceGroup02 nell'area ovest degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="50daa-115">The vault is in the resource group named ResourceGroup02 in the West US region.</span></span>
<span data-ttu-id="50daa-116">Il Vault usa il tipo di archiviazione LocallyRedundant.</span><span class="sxs-lookup"><span data-stu-id="50daa-116">The vault uses the LocallyRedundant storage type.</span></span>

## <span data-ttu-id="50daa-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50daa-117">PARAMETERS</span></span>

### <span data-ttu-id="50daa-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="50daa-118">-Name</span></span>
<span data-ttu-id="50daa-119">Specifica un nome per l'archiviazione di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="50daa-119">Specifies a name for the Azure Backup vault.</span></span>
<span data-ttu-id="50daa-120">Il nome deve essere univoco in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="50daa-120">The name must be unique in a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50daa-121">-Area geografica</span><span class="sxs-lookup"><span data-stu-id="50daa-121">-Region</span></span>
<span data-ttu-id="50daa-122">Specifica un'area di Azure in cui è presente il Vault di backup.</span><span class="sxs-lookup"><span data-stu-id="50daa-122">Specifies an Azure region in which the backup vault exists.</span></span>
<span data-ttu-id="50daa-123">Per gli scenari di backup ibridi, è consigliabile creare un Vault in un'area vicina al server locale per ridurre la latenza.</span><span class="sxs-lookup"><span data-stu-id="50daa-123">For hybrid backup scenarios, we recommend that you create a vault in a region close to the on-premise server to reduce latency.</span></span>
<span data-ttu-id="50daa-124">Per il backup delle macchine virtuali dell'infrastruttura Azure come servizio (IaaS), il Vault diventa il punto di individuazione per le macchine virtuali locali.</span><span class="sxs-lookup"><span data-stu-id="50daa-124">For backup of Azure infrastructure as a service (IaaS) virtual machines, the vault becomes the point of discovery for local virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50daa-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50daa-125">-ResourceGroupName</span></span>
<span data-ttu-id="50daa-126">Specifica il nome di un gruppo di risorse Azure esistente in cui questo cmdlet crea un Vault di backup.</span><span class="sxs-lookup"><span data-stu-id="50daa-126">Specifies the name of an existing Azure resource group in which this cmdlet creates a Backup vault.</span></span>
<span data-ttu-id="50daa-127">Per creare un gruppo di risorse, usare il cmdlet New-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="50daa-127">To create a resource group, use the New-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="50daa-128">Il gruppo risorse e il Vault di backup di Azure non devono essere nella stessa area geografica.</span><span class="sxs-lookup"><span data-stu-id="50daa-128">The resource group and the Azure Backup vault do not have to be in the same region.</span></span>

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

### <span data-ttu-id="50daa-129">-Spazio di archiviazione</span><span class="sxs-lookup"><span data-stu-id="50daa-129">-Storage</span></span>
<span data-ttu-id="50daa-130">Specifica il tipo di archiviazione per i dati di backup.</span><span class="sxs-lookup"><span data-stu-id="50daa-130">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="50daa-131">I valori accettabili per questo parametro sono: LocallyRedundant e georidondanti.</span><span class="sxs-lookup"><span data-stu-id="50daa-131">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>
<span data-ttu-id="50daa-132">Il valore predefinito è georidondante.</span><span class="sxs-lookup"><span data-stu-id="50daa-132">The default value is GeoRedundant.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases: 
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50daa-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50daa-133">-DefaultProfile</span></span>
<span data-ttu-id="50daa-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50daa-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50daa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50daa-135">CommonParameters</span></span>
<span data-ttu-id="50daa-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50daa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50daa-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50daa-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50daa-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50daa-138">INPUTS</span></span>

### <span data-ttu-id="50daa-139">Nessuno</span><span class="sxs-lookup"><span data-stu-id="50daa-139">None</span></span>

## <span data-ttu-id="50daa-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50daa-140">OUTPUTS</span></span>

### <span data-ttu-id="50daa-141">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="50daa-141">AzureRmBackupVault</span></span>

## <span data-ttu-id="50daa-142">Note</span><span class="sxs-lookup"><span data-stu-id="50daa-142">NOTES</span></span>
* <span data-ttu-id="50daa-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="50daa-143">None</span></span>

## <span data-ttu-id="50daa-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50daa-144">RELATED LINKS</span></span>

[<span data-ttu-id="50daa-145">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="50daa-145">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="50daa-146">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="50daa-146">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="50daa-147">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="50daa-147">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


