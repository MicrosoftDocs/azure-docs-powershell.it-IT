---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 5452758a5cf269ef50475b8962e5fbca117dbb1d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677540"
---
# <span data-ttu-id="54da5-101">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="54da5-101">Unregister-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="54da5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="54da5-102">SYNOPSIS</span></span>
<span data-ttu-id="54da5-103">Annulla la registrazione di un server SCDPM o di un server di backup dal Vault.</span><span class="sxs-lookup"><span data-stu-id="54da5-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

## <span data-ttu-id="54da5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="54da5-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54da5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54da5-105">DESCRIPTION</span></span>
<span data-ttu-id="54da5-106">Il cmdlet **Unregister-AzRecoveryServicesBackupManagementServer** Annulla la registrazione di un server di System Center Data Protection Manager (scdpm) o di un server di backup di Azure dalla volta.</span><span class="sxs-lookup"><span data-stu-id="54da5-106">The **Unregister-AzRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="54da5-107">Questo cmdlet consente di rimuovere i riferimenti ai server di cui è stata annullata la registrazione dal Vault.</span><span class="sxs-lookup"><span data-stu-id="54da5-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>
<span data-ttu-id="54da5-108">Prima di poter annullare la registrazione di un contenitore, è necessario eliminare tutti i dati protetti associati al contenitore.</span><span class="sxs-lookup"><span data-stu-id="54da5-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="54da5-109">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="54da5-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="54da5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="54da5-110">EXAMPLES</span></span>

### <span data-ttu-id="54da5-111">Esempio 1: annullare la registrazione di un server SCDPM dal Vault</span><span class="sxs-lookup"><span data-stu-id="54da5-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupManagementServer -AzBackupManagementServer $BMS
```

<span data-ttu-id="54da5-112">Il primo comando ottiene il server di gestione di backup denominato dpmserver01.contoso.com e lo archivia nella variabile $BMS.</span><span class="sxs-lookup"><span data-stu-id="54da5-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>
<span data-ttu-id="54da5-113">Il secondo comando Annulla la registrazione del server SCDPM dal Vault.</span><span class="sxs-lookup"><span data-stu-id="54da5-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="54da5-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="54da5-114">PARAMETERS</span></span>

### <span data-ttu-id="54da5-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="54da5-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="54da5-116">Contenitore di backup di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="54da5-116">The recovery services backup container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54da5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54da5-117">-DefaultProfile</span></span>
<span data-ttu-id="54da5-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="54da5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54da5-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54da5-119">-PassThru</span></span>
<span data-ttu-id="54da5-120">Restituire il server di gestione backup da eliminare.</span><span class="sxs-lookup"><span data-stu-id="54da5-120">Return the Backup Management Server to be deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54da5-121">-VaultId</span><span class="sxs-lookup"><span data-stu-id="54da5-121">-VaultId</span></span>
<span data-ttu-id="54da5-122">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="54da5-122">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="54da5-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="54da5-123">-Confirm</span></span>
<span data-ttu-id="54da5-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54da5-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54da5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54da5-125">-WhatIf</span></span>
<span data-ttu-id="54da5-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54da5-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54da5-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54da5-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54da5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54da5-128">CommonParameters</span></span>
<span data-ttu-id="54da5-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54da5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54da5-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54da5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54da5-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="54da5-131">INPUTS</span></span>

### <span data-ttu-id="54da5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="54da5-132">System.String</span></span>

## <span data-ttu-id="54da5-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="54da5-133">OUTPUTS</span></span>

### <span data-ttu-id="54da5-134">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="54da5-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="54da5-135">Note</span><span class="sxs-lookup"><span data-stu-id="54da5-135">NOTES</span></span>

## <span data-ttu-id="54da5-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="54da5-136">RELATED LINKS</span></span>

[<span data-ttu-id="54da5-137">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="54da5-137">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)


