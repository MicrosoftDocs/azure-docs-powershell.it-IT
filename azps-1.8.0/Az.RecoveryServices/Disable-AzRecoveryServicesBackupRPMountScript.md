---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/disable-azrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Disable-AzRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: 934f7ac105ee1164011df9bcacc672437ef4bf78
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677718"
---
# <span data-ttu-id="062fd-101">Disable-AzRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="062fd-101">Disable-AzRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="062fd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="062fd-102">SYNOPSIS</span></span>
<span data-ttu-id="062fd-103">Smonta tutti i file del punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="062fd-103">Dismounts all the files of the recovery point.</span></span>

## <span data-ttu-id="062fd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="062fd-104">SYNTAX</span></span>

```
Disable-AzRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [-PassThru]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="062fd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="062fd-105">DESCRIPTION</span></span>
<span data-ttu-id="062fd-106">Il cmdlet Disable-AzRecoveryServicesBackupRPMountScript smonta i file del punto di ripristino che sono stati montati in precedenza usando il cmdlet Get-AzRecoveryServicesBackupRPMountScript.</span><span class="sxs-lookup"><span data-stu-id="062fd-106">The Disable-AzRecoveryServicesBackupRPMountScript cmdlet dismounts the files of the recovery point which were mounted earlier using the Get-AzRecoveryServicesBackupRPMountScript cmdlet.</span></span>

## <span data-ttu-id="062fd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="062fd-107">EXAMPLES</span></span>

### <span data-ttu-id="062fd-108">Esempio 1: smontare un punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="062fd-108">Example 1: Dismount a recovery point</span></span>
```
PS C:\> $namedContainer = Get-AzRecoveryServicesBackupContainer  -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM"
PS C:\> $backupitem = Get-AzRecoveryServicesBackupItem -Container $namedContainer  -WorkloadType "AzureVM"
PS C:\> $startDate = (Get-Date).AddDays(-7)
PS C:\> $endDate = Get-Date
PS C:\> $rp = Get-AzRecoveryServicesBackupRecoveryPoint -Item $backupitem -StartDate $startdate.ToUniversalTime() -EndDate $enddate.ToUniversalTime()

To mount files of the latest recovery point, obtain the script by

PS C:\> Get-AzRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]

OsType  Password        Filename
------  --------        --------
Windows e3632984e51f496 V2VM_wus2_8287309959960546283_451516692429_cbd6061f7fc543c489f1974d33659fed07a6e0c2e08740.exe

When the script is run, it will mount the files of the recovery point $rp[0]

After the relevant files are copied, then you remove the files of the recovery point by running the disable cmdlet

PS C:\> Disable-AzRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0]
```

## <span data-ttu-id="062fd-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="062fd-109">PARAMETERS</span></span>

### <span data-ttu-id="062fd-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="062fd-110">-DefaultProfile</span></span>
<span data-ttu-id="062fd-111">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="062fd-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="062fd-112">-PassThru</span><span class="sxs-lookup"><span data-stu-id="062fd-112">-PassThru</span></span>
<span data-ttu-id="062fd-113">Restituire il punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="062fd-113">Return the recovery point.</span></span>

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

### <span data-ttu-id="062fd-114">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="062fd-114">-RecoveryPoint</span></span>
<span data-ttu-id="062fd-115">Oggetto punto di ripristino da ripristinare</span><span class="sxs-lookup"><span data-stu-id="062fd-115">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="062fd-116">-VaultId</span><span class="sxs-lookup"><span data-stu-id="062fd-116">-VaultId</span></span>
<span data-ttu-id="062fd-117">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="062fd-117">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="062fd-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="062fd-118">-Confirm</span></span>
<span data-ttu-id="062fd-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="062fd-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="062fd-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="062fd-120">-WhatIf</span></span>
<span data-ttu-id="062fd-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="062fd-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="062fd-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="062fd-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="062fd-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="062fd-123">CommonParameters</span></span>
<span data-ttu-id="062fd-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="062fd-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="062fd-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="062fd-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="062fd-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="062fd-126">INPUTS</span></span>

### <span data-ttu-id="062fd-127">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="062fd-127">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="062fd-128">System. String</span><span class="sxs-lookup"><span data-stu-id="062fd-128">System.String</span></span>

## <span data-ttu-id="062fd-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="062fd-129">OUTPUTS</span></span>

### <span data-ttu-id="062fd-130">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="062fd-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

## <span data-ttu-id="062fd-131">Note</span><span class="sxs-lookup"><span data-stu-id="062fd-131">NOTES</span></span>

## <span data-ttu-id="062fd-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="062fd-132">RELATED LINKS</span></span>
