---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: f061dc0f729709dee3bfe08bb22dba8d49a7f31b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300613"
---
# <span data-ttu-id="def21-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="def21-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="def21-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="def21-102">SYNOPSIS</span></span>

<span data-ttu-id="def21-103">Ottiene i contenitori di backup.</span><span class="sxs-lookup"><span data-stu-id="def21-103">Gets Backup containers.</span></span>

## <span data-ttu-id="def21-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="def21-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="def21-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="def21-105">DESCRIPTION</span></span>

<span data-ttu-id="def21-106">Il cmdlet **Get-AzRecoveryServicesBackupContainer** ottiene un contenitore di backup.</span><span class="sxs-lookup"><span data-stu-id="def21-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="def21-107">Un contenitore di backup incapsula le origini dati modellate come elementi di backup.</span><span class="sxs-lookup"><span data-stu-id="def21-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="def21-108">Imposta il contesto del Vault usando il parametro-VaultId.</span><span class="sxs-lookup"><span data-stu-id="def21-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="def21-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="def21-109">EXAMPLES</span></span>

### <span data-ttu-id="def21-110">Esempio 1: ottenere un contenitore specifico</span><span class="sxs-lookup"><span data-stu-id="def21-110">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="def21-111">Questo comando ottiene il contenitore denominato V2VM di tipo AzureVM.</span><span class="sxs-lookup"><span data-stu-id="def21-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="def21-112">Esempio 2: ottenere tutti i contenitori di un tipo specifico</span><span class="sxs-lookup"><span data-stu-id="def21-112">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="def21-113">Questo comando consente di ottenere tutti i contenitori Windows protetti dall'agente di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="def21-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="def21-114">Il parametro **BackupManagementType** è obbligatorio solo per i contenitori Windows.</span><span class="sxs-lookup"><span data-stu-id="def21-114">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="def21-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="def21-115">PARAMETERS</span></span>

### <span data-ttu-id="def21-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="def21-116">-BackupManagementType</span></span>

<span data-ttu-id="def21-117">Classe di risorse protette.</span><span class="sxs-lookup"><span data-stu-id="def21-117">The class of resources being protected.</span></span> <span data-ttu-id="def21-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="def21-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="def21-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="def21-119">AzureVM</span></span>
- <span data-ttu-id="def21-120">Marte</span><span class="sxs-lookup"><span data-stu-id="def21-120">MARS</span></span>
- <span data-ttu-id="def21-121">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="def21-121">AzureWorkload</span></span>
- <span data-ttu-id="def21-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="def21-122">AzureStorage</span></span>

<span data-ttu-id="def21-123">Questo parametro viene usato per distinguere i computer Windows di cui è stato eseguito il backup con l'agente MARS o altri motori di backup.</span><span class="sxs-lookup"><span data-stu-id="def21-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, AzureWorkload, AzureStorage

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def21-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="def21-124">-ContainerType</span></span>

<span data-ttu-id="def21-125">Specifica il tipo di contenitore di backup.</span><span class="sxs-lookup"><span data-stu-id="def21-125">Specifies the backup container type.</span></span>
<span data-ttu-id="def21-126">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="def21-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="def21-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="def21-127">AzureVM</span></span>
- <span data-ttu-id="def21-128">Windows</span><span class="sxs-lookup"><span data-stu-id="def21-128">Windows</span></span>
- <span data-ttu-id="def21-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="def21-129">AzureSQL</span></span>
- <span data-ttu-id="def21-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="def21-130">AzureStorage</span></span>
- <span data-ttu-id="def21-131">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="def21-131">AzureVMAppContainer</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage, AzureVMAppContainer

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def21-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="def21-132">-DefaultProfile</span></span>

<span data-ttu-id="def21-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="def21-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="def21-134">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="def21-134">-FriendlyName</span></span>

<span data-ttu-id="def21-135">Specifica il nome descrittivo del contenitore da ottenere.</span><span class="sxs-lookup"><span data-stu-id="def21-135">Specifies the friendly name of the container to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def21-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="def21-136">-ResourceGroupName</span></span>

<span data-ttu-id="def21-137">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="def21-137">Specifies the name of the resource group.</span></span>
<span data-ttu-id="def21-138">Questo parametro è solo per le macchine virtuali Azure.</span><span class="sxs-lookup"><span data-stu-id="def21-138">This parameter is for Azure virtual machines only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def21-139">-Stato</span><span class="sxs-lookup"><span data-stu-id="def21-139">-Status</span></span>

<span data-ttu-id="def21-140">Specifica lo stato di registrazione del contenitore.</span><span class="sxs-lookup"><span data-stu-id="def21-140">Specifies the container registration status.</span></span>
<span data-ttu-id="def21-141">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="def21-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="def21-142">Registrato</span><span class="sxs-lookup"><span data-stu-id="def21-142">Registered</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerRegistrationStatus
Parameter Sets: (All)
Aliases:
Accepted values: Registered

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="def21-143">-VaultId</span><span class="sxs-lookup"><span data-stu-id="def21-143">-VaultId</span></span>

<span data-ttu-id="def21-144">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="def21-144">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="def21-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="def21-145">CommonParameters</span></span>
<span data-ttu-id="def21-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="def21-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="def21-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="def21-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="def21-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="def21-148">INPUTS</span></span>

### <span data-ttu-id="def21-149">System. String</span><span class="sxs-lookup"><span data-stu-id="def21-149">System.String</span></span>

## <span data-ttu-id="def21-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="def21-150">OUTPUTS</span></span>

### <span data-ttu-id="def21-151">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="def21-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="def21-152">Note</span><span class="sxs-lookup"><span data-stu-id="def21-152">NOTES</span></span>

## <span data-ttu-id="def21-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="def21-153">RELATED LINKS</span></span>

[<span data-ttu-id="def21-154">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="def21-154">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="def21-155">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="def21-155">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="def21-156">Annullamento della registrazione-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="def21-156">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
