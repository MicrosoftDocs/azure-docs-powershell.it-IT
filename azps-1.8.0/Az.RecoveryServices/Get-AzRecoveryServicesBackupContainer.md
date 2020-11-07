---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 73438a3f294aaece7c4649f53559311d95ef4aa0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677672"
---
# <span data-ttu-id="408d0-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="408d0-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="408d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="408d0-102">SYNOPSIS</span></span>
<span data-ttu-id="408d0-103">Ottiene i contenitori di backup.</span><span class="sxs-lookup"><span data-stu-id="408d0-103">Gets Backup containers.</span></span>

## <span data-ttu-id="408d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="408d0-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="408d0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="408d0-105">DESCRIPTION</span></span>
<span data-ttu-id="408d0-106">Il cmdlet **Get-AzRecoveryServicesBackupContainer** ottiene un contenitore di backup.</span><span class="sxs-lookup"><span data-stu-id="408d0-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="408d0-107">Un contenitore di backup incapsula le origini dati modellate come elementi di backup.</span><span class="sxs-lookup"><span data-stu-id="408d0-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="408d0-108">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="408d0-108">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="408d0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="408d0-109">EXAMPLES</span></span>

### <span data-ttu-id="408d0-110">Esempio 1: ottenere un contenitore specifico</span><span class="sxs-lookup"><span data-stu-id="408d0-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="408d0-111">Questo comando ottiene il contenitore denominato V2VM di tipo AzureVM.</span><span class="sxs-lookup"><span data-stu-id="408d0-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="408d0-112">Esempio 2: ottenere tutti i contenitori di un tipo specifico</span><span class="sxs-lookup"><span data-stu-id="408d0-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="408d0-113">Questo comando consente di ottenere tutti i contenitori Windows protetti dall'agente di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="408d0-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="408d0-114">Il parametro *BackupManagementType* è obbligatorio solo per i contenitori Windows.</span><span class="sxs-lookup"><span data-stu-id="408d0-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="408d0-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="408d0-115">PARAMETERS</span></span>

### <span data-ttu-id="408d0-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="408d0-116">-BackupManagementType</span></span>
<span data-ttu-id="408d0-117">Specifica il tipo di gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="408d0-117">Specifies the backup management type.</span></span>
<span data-ttu-id="408d0-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="408d0-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="408d0-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="408d0-119">AzureVM</span></span>
- <span data-ttu-id="408d0-120">Marte</span><span class="sxs-lookup"><span data-stu-id="408d0-120">MARS</span></span>
- <span data-ttu-id="408d0-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="408d0-121">AzureSQL</span></span>
- <span data-ttu-id="408d0-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="408d0-122">AzureStorage</span></span>

<span data-ttu-id="408d0-123">Questo parametro viene usato per distinguere i computer Windows di cui è stato eseguito il backup con l'agente MARS o altri motori di backup.</span><span class="sxs-lookup"><span data-stu-id="408d0-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="408d0-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="408d0-124">-ContainerType</span></span>
<span data-ttu-id="408d0-125">Specifica il tipo di contenitore di backup.</span><span class="sxs-lookup"><span data-stu-id="408d0-125">Specifies the backup container type.</span></span>
<span data-ttu-id="408d0-126">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="408d0-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="408d0-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="408d0-127">AzureVM</span></span> 
- <span data-ttu-id="408d0-128">Windows</span><span class="sxs-lookup"><span data-stu-id="408d0-128">Windows</span></span>
- <span data-ttu-id="408d0-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="408d0-129">AzureSQL</span></span>
- <span data-ttu-id="408d0-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="408d0-130">AzureStorage</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="408d0-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="408d0-131">-DefaultProfile</span></span>
<span data-ttu-id="408d0-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="408d0-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="408d0-133">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="408d0-133">-FriendlyName</span></span>
<span data-ttu-id="408d0-134">Specifica il nome descrittivo del contenitore da ottenere.</span><span class="sxs-lookup"><span data-stu-id="408d0-134">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="408d0-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="408d0-135">-ResourceGroupName</span></span>
<span data-ttu-id="408d0-136">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="408d0-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="408d0-137">Questo parametro è solo per le macchine virtuali Azure.</span><span class="sxs-lookup"><span data-stu-id="408d0-137">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="408d0-138">-Stato</span><span class="sxs-lookup"><span data-stu-id="408d0-138">-Status</span></span>
<span data-ttu-id="408d0-139">Specifica lo stato di registrazione del contenitore.</span><span class="sxs-lookup"><span data-stu-id="408d0-139">Specifies the container registration status.</span></span>
<span data-ttu-id="408d0-140">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="408d0-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="408d0-141">Registrato</span><span class="sxs-lookup"><span data-stu-id="408d0-141">Registered</span></span>

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

### <span data-ttu-id="408d0-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="408d0-142">-VaultId</span></span>
<span data-ttu-id="408d0-143">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="408d0-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="408d0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="408d0-144">CommonParameters</span></span>
<span data-ttu-id="408d0-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="408d0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="408d0-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="408d0-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="408d0-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="408d0-147">INPUTS</span></span>

### <span data-ttu-id="408d0-148">System. String</span><span class="sxs-lookup"><span data-stu-id="408d0-148">System.String</span></span>

## <span data-ttu-id="408d0-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="408d0-149">OUTPUTS</span></span>

### <span data-ttu-id="408d0-150">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="408d0-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="408d0-151">Note</span><span class="sxs-lookup"><span data-stu-id="408d0-151">NOTES</span></span>

## <span data-ttu-id="408d0-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="408d0-152">RELATED LINKS</span></span>

[<span data-ttu-id="408d0-153">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="408d0-153">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="408d0-154">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="408d0-154">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="408d0-155">Annullamento della registrazione-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="408d0-155">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)

