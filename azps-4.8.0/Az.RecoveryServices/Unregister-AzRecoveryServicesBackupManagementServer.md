---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: cc52435ff0b288656e4a917620659737f33916ca
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032822"
---
# <span data-ttu-id="91d82-101">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="91d82-101">Unregister-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="91d82-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91d82-102">SYNOPSIS</span></span>
<span data-ttu-id="91d82-103">Annulla la registrazione di un server SCDPM o di un server di backup dal Vault.</span><span class="sxs-lookup"><span data-stu-id="91d82-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

## <span data-ttu-id="91d82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91d82-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91d82-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91d82-105">DESCRIPTION</span></span>
<span data-ttu-id="91d82-106">Il cmdlet **Unregister-AzRecoveryServicesBackupManagementServer** Annulla la registrazione di un server di System Center Data Protection Manager (scdpm) o di un server di backup di Azure dalla volta.</span><span class="sxs-lookup"><span data-stu-id="91d82-106">The **Unregister-AzRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="91d82-107">Questo cmdlet consente di rimuovere i riferimenti ai server di cui è stata annullata la registrazione dal Vault.</span><span class="sxs-lookup"><span data-stu-id="91d82-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>
<span data-ttu-id="91d82-108">Prima di poter annullare la registrazione di un contenitore, è necessario eliminare tutti i dati protetti associati al contenitore.</span><span class="sxs-lookup"><span data-stu-id="91d82-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="91d82-109">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="91d82-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="91d82-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91d82-110">EXAMPLES</span></span>

### <span data-ttu-id="91d82-111">Esempio 1: annullare la registrazione di un server SCDPM dal Vault</span><span class="sxs-lookup"><span data-stu-id="91d82-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```powershell
PS C:\>$BMS = Get-AzRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupManagementServer -AzBackupManagementServer $BMS
```

<span data-ttu-id="91d82-112">Il primo comando ottiene il server di gestione di backup denominato dpmserver01.contoso.com e lo archivia nella variabile $BMS.</span><span class="sxs-lookup"><span data-stu-id="91d82-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>
<span data-ttu-id="91d82-113">Il secondo comando Annulla la registrazione del server SCDPM dal Vault.</span><span class="sxs-lookup"><span data-stu-id="91d82-113">The second command unregisters the SCDPM server from the vault.</span></span>

### <span data-ttu-id="91d82-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="91d82-114">Example 2</span></span>

<span data-ttu-id="91d82-115">Annulla la registrazione di un server SCDPM o di un server di backup dal Vault.</span><span class="sxs-lookup"><span data-stu-id="91d82-115">Unregisters a SCDPM server or Backup server from the vault.</span></span> <span data-ttu-id="91d82-116">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="91d82-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Unregister-AzRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer <BackupEngineBase> -VaultId $vault.ID
```

## <span data-ttu-id="91d82-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91d82-117">PARAMETERS</span></span>

### <span data-ttu-id="91d82-118">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="91d82-118">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="91d82-119">Contenitore di backup di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="91d82-119">The recovery services backup container.</span></span>

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

### <span data-ttu-id="91d82-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91d82-120">-DefaultProfile</span></span>
<span data-ttu-id="91d82-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91d82-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91d82-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="91d82-122">-PassThru</span></span>
<span data-ttu-id="91d82-123">Restituire il server di gestione backup da eliminare.</span><span class="sxs-lookup"><span data-stu-id="91d82-123">Return the Backup Management Server to be deleted.</span></span>

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

### <span data-ttu-id="91d82-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="91d82-124">-VaultId</span></span>
<span data-ttu-id="91d82-125">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="91d82-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="91d82-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="91d82-126">-Confirm</span></span>
<span data-ttu-id="91d82-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91d82-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91d82-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91d82-128">-WhatIf</span></span>
<span data-ttu-id="91d82-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91d82-129">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="91d82-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91d82-130">CommonParameters</span></span>
<span data-ttu-id="91d82-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91d82-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91d82-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91d82-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91d82-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91d82-133">INPUTS</span></span>

### <span data-ttu-id="91d82-134">System. String</span><span class="sxs-lookup"><span data-stu-id="91d82-134">System.String</span></span>

## <span data-ttu-id="91d82-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91d82-135">OUTPUTS</span></span>

### <span data-ttu-id="91d82-136">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="91d82-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="91d82-137">Note</span><span class="sxs-lookup"><span data-stu-id="91d82-137">NOTES</span></span>

## <span data-ttu-id="91d82-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91d82-138">RELATED LINKS</span></span>

[<span data-ttu-id="91d82-139">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="91d82-139">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)


