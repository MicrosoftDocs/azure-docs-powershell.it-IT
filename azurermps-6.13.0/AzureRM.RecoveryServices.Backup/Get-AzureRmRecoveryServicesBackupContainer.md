---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: c47c3e51d970302281af5a7ae3a6175f4af79739
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687279"
---
# <span data-ttu-id="4157b-101">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="4157b-101">Get-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="4157b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4157b-102">SYNOPSIS</span></span>
<span data-ttu-id="4157b-103">Ottiene i contenitori di backup.</span><span class="sxs-lookup"><span data-stu-id="4157b-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4157b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4157b-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-Name] <String>] [[-FriendlyName] <String>] [[-ResourceGroupName] <String>]
 [[-Status] <ContainerRegistrationStatus>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4157b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4157b-105">DESCRIPTION</span></span>
<span data-ttu-id="4157b-106">Il cmdlet **Get-AzureRmRecoveryServicesBackupContainer** ottiene un contenitore di backup.</span><span class="sxs-lookup"><span data-stu-id="4157b-106">The **Get-AzureRmRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="4157b-107">Un contenitore di backup incapsula le origini dati modellate come elementi di backup.</span><span class="sxs-lookup"><span data-stu-id="4157b-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="4157b-108">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="4157b-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="4157b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4157b-109">EXAMPLES</span></span>

### <span data-ttu-id="4157b-110">Esempio 1: ottenere un contenitore specifico</span><span class="sxs-lookup"><span data-stu-id="4157b-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="4157b-111">Questo comando ottiene il contenitore denominato V2VM di tipo AzureVM.</span><span class="sxs-lookup"><span data-stu-id="4157b-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="4157b-112">Esempio 2: ottenere tutti i contenitori di un tipo specifico</span><span class="sxs-lookup"><span data-stu-id="4157b-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="4157b-113">Questo comando consente di ottenere tutti i contenitori Windows protetti dall'agente di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="4157b-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="4157b-114">Il parametro *BackupManagementType* è obbligatorio solo per i contenitori Windows.</span><span class="sxs-lookup"><span data-stu-id="4157b-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="4157b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4157b-115">PARAMETERS</span></span>

### <span data-ttu-id="4157b-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="4157b-116">-BackupManagementType</span></span>
<span data-ttu-id="4157b-117">Specifica il tipo di gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="4157b-117">Specifies the backup management type.</span></span>
<span data-ttu-id="4157b-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4157b-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4157b-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="4157b-119">AzureVM</span></span>
- <span data-ttu-id="4157b-120">Marte</span><span class="sxs-lookup"><span data-stu-id="4157b-120">MARS</span></span>
- <span data-ttu-id="4157b-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="4157b-121">AzureSQL</span></span>
- <span data-ttu-id="4157b-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="4157b-122">AzureStorage</span></span>

<span data-ttu-id="4157b-123">Questo parametro viene usato per distinguere i computer Windows di cui è stato eseguito il backup con l'agente MARS o altri motori di backup.</span><span class="sxs-lookup"><span data-stu-id="4157b-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, AzureSQL, AzureStorage

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4157b-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="4157b-124">-ContainerType</span></span>
<span data-ttu-id="4157b-125">Specifica il tipo di contenitore di backup.</span><span class="sxs-lookup"><span data-stu-id="4157b-125">Specifies the backup container type.</span></span>
<span data-ttu-id="4157b-126">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4157b-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4157b-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="4157b-127">AzureVM</span></span> 
- <span data-ttu-id="4157b-128">Windows</span><span class="sxs-lookup"><span data-stu-id="4157b-128">Windows</span></span>
- <span data-ttu-id="4157b-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="4157b-129">AzureSQL</span></span>
- <span data-ttu-id="4157b-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="4157b-130">AzureStorage</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4157b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4157b-131">-DefaultProfile</span></span>
<span data-ttu-id="4157b-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4157b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4157b-133">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4157b-133">-FriendlyName</span></span>
<span data-ttu-id="4157b-134">Specifica il nome descrittivo del contenitore da ottenere.</span><span class="sxs-lookup"><span data-stu-id="4157b-134">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="4157b-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="4157b-135">-Name</span></span>
<span data-ttu-id="4157b-136">Specifica il nome del contenitore da ottenere.</span><span class="sxs-lookup"><span data-stu-id="4157b-136">Specifies the name of the container to get.</span></span>

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

### <span data-ttu-id="4157b-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4157b-137">-ResourceGroupName</span></span>
<span data-ttu-id="4157b-138">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4157b-138">Specifies the name of the resource group.</span></span>
<span data-ttu-id="4157b-139">Questo parametro è solo per le macchine virtuali Azure.</span><span class="sxs-lookup"><span data-stu-id="4157b-139">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="4157b-140">-Stato</span><span class="sxs-lookup"><span data-stu-id="4157b-140">-Status</span></span>
<span data-ttu-id="4157b-141">Specifica lo stato di registrazione del contenitore.</span><span class="sxs-lookup"><span data-stu-id="4157b-141">Specifies the container registration status.</span></span>
<span data-ttu-id="4157b-142">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="4157b-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4157b-143">Registrato</span><span class="sxs-lookup"><span data-stu-id="4157b-143">Registered</span></span>

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

### <span data-ttu-id="4157b-144">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4157b-144">-VaultId</span></span>
<span data-ttu-id="4157b-145">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="4157b-145">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4157b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4157b-146">CommonParameters</span></span>
<span data-ttu-id="4157b-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4157b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4157b-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4157b-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4157b-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4157b-149">INPUTS</span></span>

### <span data-ttu-id="4157b-150">System. String</span><span class="sxs-lookup"><span data-stu-id="4157b-150">System.String</span></span>
<span data-ttu-id="4157b-151">Parametri: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4157b-151">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="4157b-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4157b-152">OUTPUTS</span></span>

### <span data-ttu-id="4157b-153">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="4157b-153">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="4157b-154">Note</span><span class="sxs-lookup"><span data-stu-id="4157b-154">NOTES</span></span>

## <span data-ttu-id="4157b-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4157b-155">RELATED LINKS</span></span>

[<span data-ttu-id="4157b-156">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4157b-156">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="4157b-157">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="4157b-157">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="4157b-158">Annullamento della registrazione-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="4157b-158">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>](./Unregister-AzureRmRecoveryServicesBackupContainer.md)


