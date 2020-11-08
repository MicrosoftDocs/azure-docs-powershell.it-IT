---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprpmountscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRPMountScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRPMountScript.md
ms.openlocfilehash: c408367a2bf7ce1c127b87275ccaea7233f176c3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191321"
---
# <span data-ttu-id="31a2c-101">Get-AzRecoveryServicesBackupRPMountScript</span><span class="sxs-lookup"><span data-stu-id="31a2c-101">Get-AzRecoveryServicesBackupRPMountScript</span></span>

## <span data-ttu-id="31a2c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31a2c-102">SYNOPSIS</span></span>
<span data-ttu-id="31a2c-103">Scarica uno script per montare tutti i file del punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="31a2c-103">Downloads a script to mount all the files of the recovery point.</span></span>

## <span data-ttu-id="31a2c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31a2c-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupRPMountScript [-RecoveryPoint] <RecoveryPointBase> [[-Path] <String>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31a2c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31a2c-105">DESCRIPTION</span></span>
<span data-ttu-id="31a2c-106">Il cmdlet Get-AzRecoveryServicesBackupRPMountScript Scarica uno script che monta i volumi del punto di recupero nel computer in cui viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31a2c-106">The Get-AzRecoveryServicesBackupRPMountScript cmdlet downloads a script which mounts the volumes of the recovery point on the machine where it is run.</span></span>

## <span data-ttu-id="31a2c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31a2c-107">EXAMPLES</span></span>

### <span data-ttu-id="31a2c-108">Esempio 1: montare un punto di ripristino</span><span class="sxs-lookup"><span data-stu-id="31a2c-108">Example 1: Mount a recovery point</span></span>
```powershell
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
```

<span data-ttu-id="31a2c-109">Quando lo script viene eseguito, verranno montati i file del punto di ripristino $rp \[ 0\]</span><span class="sxs-lookup"><span data-stu-id="31a2c-109">When the script is run, it will mount the files of the recovery point $rp\[0\]</span></span>

### <span data-ttu-id="31a2c-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="31a2c-110">Example 2</span></span>

<span data-ttu-id="31a2c-111">Scarica uno script per montare tutti i file del punto di ripristino.</span><span class="sxs-lookup"><span data-stu-id="31a2c-111">Downloads a script to mount all the files of the recovery point.</span></span> <span data-ttu-id="31a2c-112">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="31a2c-112">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRPMountScript -RecoveryPoint $rp[0] -VaultId $vault.ID
```

## <span data-ttu-id="31a2c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31a2c-113">PARAMETERS</span></span>

### <span data-ttu-id="31a2c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31a2c-114">-DefaultProfile</span></span>
<span data-ttu-id="31a2c-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31a2c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31a2c-116">-Path</span><span class="sxs-lookup"><span data-stu-id="31a2c-116">-Path</span></span>
<span data-ttu-id="31a2c-117">Posizione in cui il file deve essere scaricato in caso di recupero file.</span><span class="sxs-lookup"><span data-stu-id="31a2c-117">Location where the file should be downloaded in the case of file recovery.</span></span> <span data-ttu-id="31a2c-118">Se-path non è disponibile, il file di script verrà scaricato nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="31a2c-118">If -Path is not provided, the script file will be downloaded in the current directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31a2c-119">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="31a2c-119">-RecoveryPoint</span></span>
<span data-ttu-id="31a2c-120">Oggetto punto di ripristino da ripristinare</span><span class="sxs-lookup"><span data-stu-id="31a2c-120">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="31a2c-121">-VaultId</span><span class="sxs-lookup"><span data-stu-id="31a2c-121">-VaultId</span></span>
<span data-ttu-id="31a2c-122">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="31a2c-122">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="31a2c-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="31a2c-123">-Confirm</span></span>
<span data-ttu-id="31a2c-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31a2c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31a2c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31a2c-125">-WhatIf</span></span>
<span data-ttu-id="31a2c-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31a2c-126">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="31a2c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a2c-127">CommonParameters</span></span>
<span data-ttu-id="31a2c-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31a2c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a2c-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31a2c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a2c-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31a2c-130">INPUTS</span></span>

### <span data-ttu-id="31a2c-131">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="31a2c-131">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>

### <span data-ttu-id="31a2c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="31a2c-132">System.String</span></span>

## <span data-ttu-id="31a2c-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31a2c-133">OUTPUTS</span></span>

### <span data-ttu-id="31a2c-134">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. RPMountScriptDetails</span><span class="sxs-lookup"><span data-stu-id="31a2c-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RPMountScriptDetails</span></span>

## <span data-ttu-id="31a2c-135">Note</span><span class="sxs-lookup"><span data-stu-id="31a2c-135">NOTES</span></span>

## <span data-ttu-id="31a2c-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31a2c-136">RELATED LINKS</span></span>