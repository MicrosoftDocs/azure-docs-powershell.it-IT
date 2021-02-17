---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: bd4945436c840323121be7a4450a0042acf67cde
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183935"
---
# <span data-ttu-id="f7b16-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f7b16-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="f7b16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7b16-102">SYNOPSIS</span></span>

<span data-ttu-id="f7b16-103">Recupera i contenitori di backup.</span><span class="sxs-lookup"><span data-stu-id="f7b16-103">Gets Backup containers.</span></span>

## <span data-ttu-id="f7b16-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7b16-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7b16-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f7b16-105">DESCRIPTION</span></span>

<span data-ttu-id="f7b16-106">Il cmdlet **Get-AzRecoveryServicesBackupContainer** ottiene un contenitore di backup.</span><span class="sxs-lookup"><span data-stu-id="f7b16-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span> <span data-ttu-id="f7b16-107">Un contenitore di backup incapsula le origini dati modellate come elementi di backup.</span><span class="sxs-lookup"><span data-stu-id="f7b16-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="f7b16-108">Per il tipo di contenitore "Azure VM", l'output elenca tutti i contenitori il cui nome corrisponde esattamente a quello passato come valore per il parametro Nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="f7b16-108">For Container type "Azure VM" , the output lists all the containers whose name exactly matches to the one passed  as the value for Friendly Name parameter.</span></span> <span data-ttu-id="f7b16-109">Per altri tipi di contenitori, l'output fornisce un elenco di contenitori con un nome simile al valore passato per il parametro nome descrittivo.</span><span class="sxs-lookup"><span data-stu-id="f7b16-109">For other container types,  output gives a list of containers with name similar to the value passed for Friendly name parameter.</span></span>
<span data-ttu-id="f7b16-110">Impostare il contesto del vault usando il parametro -VaultId.</span><span class="sxs-lookup"><span data-stu-id="f7b16-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="f7b16-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7b16-111">EXAMPLES</span></span>

### <span data-ttu-id="f7b16-112">Esempio 1: Ottenere un contenitore specifico</span><span class="sxs-lookup"><span data-stu-id="f7b16-112">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="f7b16-113">Questo comando recupera il contenitore denominato V2VM di tipo AzureVM.</span><span class="sxs-lookup"><span data-stu-id="f7b16-113">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="f7b16-114">Esempio 2: Ottenere tutti i contenitori di un tipo specifico</span><span class="sxs-lookup"><span data-stu-id="f7b16-114">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="f7b16-115">Questo comando recupera tutti i contenitori di Windows protetti dall'agente di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="f7b16-115">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="f7b16-116">Il **parametro BackupManagementType** è necessario solo per i contenitori di Windows.</span><span class="sxs-lookup"><span data-stu-id="f7b16-116">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="f7b16-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7b16-117">PARAMETERS</span></span>

### <span data-ttu-id="f7b16-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="f7b16-118">-BackupManagementType</span></span>

<span data-ttu-id="f7b16-119">Classe di risorse protetta.</span><span class="sxs-lookup"><span data-stu-id="f7b16-119">The class of resources being protected.</span></span> <span data-ttu-id="f7b16-120">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="f7b16-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f7b16-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="f7b16-121">AzureVM</span></span>
- <span data-ttu-id="f7b16-122">MARS</span><span class="sxs-lookup"><span data-stu-id="f7b16-122">MARS</span></span>
- <span data-ttu-id="f7b16-123">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="f7b16-123">AzureWorkload</span></span>
- <span data-ttu-id="f7b16-124">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="f7b16-124">AzureStorage</span></span>

<span data-ttu-id="f7b16-125">Questo parametro viene usato per differenziare i computer Windows di cui viene eseguito il backup usando l'agente MARS o altri motori di backup.</span><span class="sxs-lookup"><span data-stu-id="f7b16-125">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="f7b16-126">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="f7b16-126">-ContainerType</span></span>

<span data-ttu-id="f7b16-127">Specifica il tipo di contenitore di backup.</span><span class="sxs-lookup"><span data-stu-id="f7b16-127">Specifies the backup container type.</span></span>
<span data-ttu-id="f7b16-128">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="f7b16-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f7b16-129">AzureVM</span><span class="sxs-lookup"><span data-stu-id="f7b16-129">AzureVM</span></span>
- <span data-ttu-id="f7b16-130">Windows</span><span class="sxs-lookup"><span data-stu-id="f7b16-130">Windows</span></span>
- <span data-ttu-id="f7b16-131">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="f7b16-131">AzureStorage</span></span>
- <span data-ttu-id="f7b16-132">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="f7b16-132">AzureVMAppContainer</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureStorage, AzureVMAppContainer

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7b16-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7b16-133">-DefaultProfile</span></span>

<span data-ttu-id="f7b16-134">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7b16-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7b16-135">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f7b16-135">-FriendlyName</span></span>

<span data-ttu-id="f7b16-136">Specifica il nome descrittivo del contenitore da ottenere.</span><span class="sxs-lookup"><span data-stu-id="f7b16-136">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="f7b16-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7b16-137">-ResourceGroupName</span></span>

<span data-ttu-id="f7b16-138">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7b16-138">Specifies the name of the resource group.</span></span>
<span data-ttu-id="f7b16-139">Questo parametro è valido solo per le macchine virtuali di Azure.</span><span class="sxs-lookup"><span data-stu-id="f7b16-139">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="f7b16-140">-Stato</span><span class="sxs-lookup"><span data-stu-id="f7b16-140">-Status</span></span>

<span data-ttu-id="f7b16-141">Specifica lo stato di registrazione del contenitore.</span><span class="sxs-lookup"><span data-stu-id="f7b16-141">Specifies the container registration status.</span></span>
<span data-ttu-id="f7b16-142">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="f7b16-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f7b16-143">Registrata</span><span class="sxs-lookup"><span data-stu-id="f7b16-143">Registered</span></span>

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

### <span data-ttu-id="f7b16-144">-VaultId</span><span class="sxs-lookup"><span data-stu-id="f7b16-144">-VaultId</span></span>

<span data-ttu-id="f7b16-145">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="f7b16-145">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="f7b16-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b16-146">CommonParameters</span></span>
<span data-ttu-id="f7b16-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7b16-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b16-148">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f7b16-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b16-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="f7b16-149">INPUTS</span></span>

### <span data-ttu-id="f7b16-150">System.String</span><span class="sxs-lookup"><span data-stu-id="f7b16-150">System.String</span></span>

## <span data-ttu-id="f7b16-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7b16-151">OUTPUTS</span></span>

### <span data-ttu-id="f7b16-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="f7b16-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="f7b16-153">NOTE</span><span class="sxs-lookup"><span data-stu-id="f7b16-153">NOTES</span></span>

## <span data-ttu-id="f7b16-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7b16-154">RELATED LINKS</span></span>

[<span data-ttu-id="f7b16-155">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="f7b16-155">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="f7b16-156">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="f7b16-156">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="f7b16-157">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="f7b16-157">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
