---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/disable-azurermrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Disable-AzureRmRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: bcb3da6f7425f759ab8d4142e5c62a8aa68e85e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685759"
---
# <span data-ttu-id="5cefc-101">Disable-AzureRmRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="5cefc-101">Disable-AzureRmRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="5cefc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5cefc-102">SYNOPSIS</span></span>
<span data-ttu-id="5cefc-103">Smonta tutti i file del punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5cefc-103">Dismounts all the files of the recovery point.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cefc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5cefc-104">SYNTAX</span></span>

```
Disable-AzureRmRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [-PassThru]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cefc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5cefc-105">DESCRIPTION</span></span>
<span data-ttu-id="5cefc-106">Il cmdlet Disable-AzureRmRecoveryServicesBackupRPMountScript smonta i file del punto di ripristino che sono stati montati in precedenza usando il cmdlet Get-AzureRmRecoveryServicesBackupRPMountScript.</span><span class="sxs-lookup"><span data-stu-id="5cefc-106">The Disable-AzureRmRecoveryServicesBackupRPMountScript cmdlet dismounts the files of the recovery point which were mounted earlier using the Get-AzureRmRecoveryServicesBackupRPMountScript cmdlet.</span></span>

## <span data-ttu-id="5cefc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5cefc-107">EXAMPLES</span></span>

### <span data-ttu-id="5cefc-108">Esempio 1: smontare un punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="5cefc-108">Example 1: Dismount a recovery point</span></span>
```
PS C:\> $namedContainer = Get-AzureRmRecoveryServicesBackupContainer  -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM"
PS C:\> $backupitem = Get-AzureRmRecoveryServicesBackupItem -Container $namedContainer  -WorkloadType "AzureVM"
PS C:\> $startDate = (Get-Date).AddDays(-7)
PS C:\> $endDate = Get-Date
PS C:\> $rp = Get-AzureRmRecoveryServicesBackupRecoveryPoint -Item $backupitem -StartDate $startdate.ToUniversalTime() -EndDate $enddate.ToUniversalTime()

To mount files of the latest recovery point, obtain the script by

PS C:\> Get-AzureRmRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]

OsType  Password        Filename
------  --------        --------
Windows e3632984e51f496 V2VM_wus2_8287309959960546283_451516692429_cbd6061f7fc543c489f1974d33659fed07a6e0c2e08740.exe

When the script is run, it will mount the files of the recovery point $rp[0]

After the relevant files are copied, then you remove the files of the recovery point by running the disable cmdlet

PS C:\> Disable-AzureRmRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]
```

## <span data-ttu-id="5cefc-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5cefc-109">PARAMETERS</span></span>

### <span data-ttu-id="5cefc-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cefc-110">-DefaultProfile</span></span>
<span data-ttu-id="5cefc-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5cefc-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cefc-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5cefc-112">-PassThru</span></span>
<span data-ttu-id="5cefc-113">Restituire il punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5cefc-113">Return the recovery point.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cefc-114">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="5cefc-114">-RecoveryPoint</span></span>
<span data-ttu-id="5cefc-115">Oggetto punto di ripristino da ripristinare</span><span class="sxs-lookup"><span data-stu-id="5cefc-115">Recovery point object to be restored</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cefc-116">-VaultId</span><span class="sxs-lookup"><span data-stu-id="5cefc-116">-VaultId</span></span>
<span data-ttu-id="5cefc-117">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5cefc-117">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5cefc-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5cefc-118">-Confirm</span></span>
<span data-ttu-id="5cefc-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cefc-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cefc-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cefc-120">-WhatIf</span></span>
<span data-ttu-id="5cefc-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5cefc-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5cefc-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5cefc-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cefc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cefc-123">CommonParameters</span></span>
<span data-ttu-id="5cefc-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cefc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cefc-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cefc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cefc-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5cefc-126">INPUTS</span></span>

### <span data-ttu-id="5cefc-127">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="5cefc-127">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="5cefc-128">Parametri: RecoveryPoint (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5cefc-128">Parameters: RecoveryPoint (ByValue)</span></span>

### <span data-ttu-id="5cefc-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5cefc-129">System.String</span></span>
<span data-ttu-id="5cefc-130">Parametri: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5cefc-130">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="5cefc-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5cefc-131">OUTPUTS</span></span>

### <span data-ttu-id="5cefc-132">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="5cefc-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="5cefc-133">Note</span><span class="sxs-lookup"><span data-stu-id="5cefc-133">NOTES</span></span>

## <span data-ttu-id="5cefc-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5cefc-134">RELATED LINKS</span></span>
