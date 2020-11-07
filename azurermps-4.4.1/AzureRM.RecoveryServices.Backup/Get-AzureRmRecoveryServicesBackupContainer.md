---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: e6b0633b43bc93c516c9c5b6f4872ecbd6d68520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687997"
---
# <span data-ttu-id="bce63-101">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="bce63-101">Get-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="bce63-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bce63-102">SYNOPSIS</span></span>
<span data-ttu-id="bce63-103">Ottiene i contenitori di backup.</span><span class="sxs-lookup"><span data-stu-id="bce63-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bce63-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bce63-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-Name] <String>] [[-FriendlyName] <String>] [[-ResourceGroupName] <String>]
 [[-Status] <ContainerRegistrationStatus>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bce63-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bce63-105">DESCRIPTION</span></span>
<span data-ttu-id="bce63-106">Il cmdlet **Get-AzureRmRecoveryServicesBackupContainer** ottiene un contenitore di backup.</span><span class="sxs-lookup"><span data-stu-id="bce63-106">The **Get-AzureRmRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="bce63-107">Un contenitore di backup incapsula le origini dati modellate come elementi di backup.</span><span class="sxs-lookup"><span data-stu-id="bce63-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>

<span data-ttu-id="bce63-108">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="bce63-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="bce63-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bce63-109">EXAMPLES</span></span>

### <span data-ttu-id="bce63-110">Esempio 1: ottenere un contenitore specifico</span><span class="sxs-lookup"><span data-stu-id="bce63-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="bce63-111">Questo comando ottiene il contenitore denominato V2VM di tipo AzureVM.</span><span class="sxs-lookup"><span data-stu-id="bce63-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="bce63-112">Esempio 2: ottenere tutti i contenitori di un tipo specifico</span><span class="sxs-lookup"><span data-stu-id="bce63-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="bce63-113">Questo comando consente di ottenere tutti i contenitori Windows protetti dall'agente di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="bce63-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="bce63-114">Il parametro *BackupManagementType* è obbligatorio solo per i contenitori Windows.</span><span class="sxs-lookup"><span data-stu-id="bce63-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="bce63-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bce63-115">PARAMETERS</span></span>

### <span data-ttu-id="bce63-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="bce63-116">-BackupManagementType</span></span>
<span data-ttu-id="bce63-117">Specifica il tipo di gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="bce63-117">Specifies the backup management type.</span></span>
<span data-ttu-id="bce63-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="bce63-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bce63-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="bce63-119">AzureVM</span></span>
- <span data-ttu-id="bce63-120">Marte</span><span class="sxs-lookup"><span data-stu-id="bce63-120">MARS</span></span>
- <span data-ttu-id="bce63-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="bce63-121">AzureSQL</span></span>

<span data-ttu-id="bce63-122">Questo parametro viene usato per distinguere i computer Windows di cui è stato eseguito il backup con l'agente MARS o altri motori di backup.</span><span class="sxs-lookup"><span data-stu-id="bce63-122">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, AzureSQL

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce63-123">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="bce63-123">-ContainerType</span></span>
<span data-ttu-id="bce63-124">Specifica il tipo di contenitore di backup.</span><span class="sxs-lookup"><span data-stu-id="bce63-124">Specifies the backup container type.</span></span>
<span data-ttu-id="bce63-125">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="bce63-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bce63-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="bce63-126">AzureVM</span></span> 
- <span data-ttu-id="bce63-127">Windows</span><span class="sxs-lookup"><span data-stu-id="bce63-127">Windows</span></span>
- <span data-ttu-id="bce63-128">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="bce63-128">AzureSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, Windows, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bce63-129">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="bce63-129">-FriendlyName</span></span>
<span data-ttu-id="bce63-130">Specifica il nome descrittivo del contenitore da ottenere.</span><span class="sxs-lookup"><span data-stu-id="bce63-130">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="bce63-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="bce63-131">-Name</span></span>
<span data-ttu-id="bce63-132">Specifica il nome del contenitore da ottenere.</span><span class="sxs-lookup"><span data-stu-id="bce63-132">Specifies the name of the container to get.</span></span>

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

### <span data-ttu-id="bce63-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bce63-133">-ResourceGroupName</span></span>
<span data-ttu-id="bce63-134">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bce63-134">Specifies the name of the resource group.</span></span>
<span data-ttu-id="bce63-135">Questo parametro è solo per le macchine virtuali Azure.</span><span class="sxs-lookup"><span data-stu-id="bce63-135">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="bce63-136">-Stato</span><span class="sxs-lookup"><span data-stu-id="bce63-136">-Status</span></span>
<span data-ttu-id="bce63-137">Specifica lo stato di registrazione del contenitore.</span><span class="sxs-lookup"><span data-stu-id="bce63-137">Specifies the container registration status.</span></span>
<span data-ttu-id="bce63-138">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="bce63-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bce63-139">Registrato</span><span class="sxs-lookup"><span data-stu-id="bce63-139">Registered</span></span>

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

### <span data-ttu-id="bce63-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bce63-140">-DefaultProfile</span></span>
<span data-ttu-id="bce63-141">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bce63-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bce63-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bce63-142">CommonParameters</span></span>
<span data-ttu-id="bce63-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bce63-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bce63-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bce63-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bce63-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bce63-145">INPUTS</span></span>

## <span data-ttu-id="bce63-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bce63-146">OUTPUTS</span></span>

### <span data-ttu-id="bce63-147">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="bce63-147">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="bce63-148">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ContainerBase]</span><span class="sxs-lookup"><span data-stu-id="bce63-148">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase]</span></span>

## <span data-ttu-id="bce63-149">Note</span><span class="sxs-lookup"><span data-stu-id="bce63-149">NOTES</span></span>

## <span data-ttu-id="bce63-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bce63-150">RELATED LINKS</span></span>

[<span data-ttu-id="bce63-151">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="bce63-151">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="bce63-152">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="bce63-152">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="bce63-153">Annullamento della registrazione-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="bce63-153">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>](./Unregister-AzureRmRecoveryServicesBackupContainer.md)


