---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/unregister-azurermrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 4ef306b80aaf5fbb03b5ee4e98104829d8853ba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686369"
---
# <span data-ttu-id="0e465-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="0e465-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="0e465-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0e465-102">SYNOPSIS</span></span>
<span data-ttu-id="0e465-103">Annulla la registrazione di un server SCDPM o di un server di backup dal Vault.</span><span class="sxs-lookup"><span data-stu-id="0e465-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e465-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0e465-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0e465-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e465-105">DESCRIPTION</span></span>
<span data-ttu-id="0e465-106">Il cmdlet **Unregister-AzureRmRecoveryServicesBackupManagementServer** Annulla la registrazione di un server di System Center Data Protection Manager (scdpm) o di un server di backup di Azure dalla volta.</span><span class="sxs-lookup"><span data-stu-id="0e465-106">The **Unregister-AzureRmRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="0e465-107">Questo cmdlet consente di rimuovere i riferimenti ai server di cui è stata annullata la registrazione dal Vault.</span><span class="sxs-lookup"><span data-stu-id="0e465-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>
<span data-ttu-id="0e465-108">Prima di poter annullare la registrazione di un contenitore, è necessario eliminare tutti i dati protetti associati al contenitore.</span><span class="sxs-lookup"><span data-stu-id="0e465-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="0e465-109">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="0e465-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="0e465-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0e465-110">EXAMPLES</span></span>

### <span data-ttu-id="0e465-111">Esempio 1: annullare la registrazione di un server SCDPM dal Vault</span><span class="sxs-lookup"><span data-stu-id="0e465-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzureRmRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer $BMS
```

<span data-ttu-id="0e465-112">Il primo comando ottiene il server di gestione di backup denominato dpmserver01.contoso.com e lo archivia nella variabile $BMS.</span><span class="sxs-lookup"><span data-stu-id="0e465-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>
<span data-ttu-id="0e465-113">Il secondo comando Annulla la registrazione del server SCDPM dal Vault.</span><span class="sxs-lookup"><span data-stu-id="0e465-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="0e465-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0e465-114">PARAMETERS</span></span>

### <span data-ttu-id="0e465-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="0e465-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="0e465-116">Specifica un oggetto server SCDPM per annullare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="0e465-116">Specifies an SCDPM server object to unregister.</span></span>
<span data-ttu-id="0e465-117">Per ottenere un oggetto **BackupManagementServer** , usa il cmdlet Get-AzureRmRecoveryServicesBackupManagementServer.</span><span class="sxs-lookup"><span data-stu-id="0e465-117">To obtain an **BackupManagementServer** object, use the Get-AzureRmRecoveryServicesBackupManagementServer cmdlet.</span></span>

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

### <span data-ttu-id="0e465-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e465-118">-DefaultProfile</span></span>
<span data-ttu-id="0e465-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0e465-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e465-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e465-120">-PassThru</span></span>
<span data-ttu-id="0e465-121">Restituire il server di gestione backup da eliminare.</span><span class="sxs-lookup"><span data-stu-id="0e465-121">Return the Backup Management Server to be deleted.</span></span>

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

### <span data-ttu-id="0e465-122">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0e465-122">-VaultId</span></span>
<span data-ttu-id="0e465-123">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0e465-123">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0e465-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0e465-124">-Confirm</span></span>
<span data-ttu-id="0e465-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e465-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e465-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e465-126">-WhatIf</span></span>
<span data-ttu-id="0e465-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0e465-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e465-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0e465-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e465-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e465-129">CommonParameters</span></span>
<span data-ttu-id="0e465-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e465-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e465-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e465-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e465-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0e465-132">INPUTS</span></span>

### <span data-ttu-id="0e465-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0e465-133">System.String</span></span>
<span data-ttu-id="0e465-134">Parametri: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0e465-134">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="0e465-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0e465-135">OUTPUTS</span></span>

### <span data-ttu-id="0e465-136">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="0e465-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="0e465-137">Note</span><span class="sxs-lookup"><span data-stu-id="0e465-137">NOTES</span></span>

## <span data-ttu-id="0e465-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0e465-138">RELATED LINKS</span></span>

[<span data-ttu-id="0e465-139">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="0e465-139">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)


