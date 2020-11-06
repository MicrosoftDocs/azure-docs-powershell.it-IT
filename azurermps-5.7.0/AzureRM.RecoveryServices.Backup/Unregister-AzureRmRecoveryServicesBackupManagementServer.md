---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/unregister-azurermrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 7612a816db41e3befb58cc739bcc78e2d27ec8d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509700"
---
# <span data-ttu-id="c8298-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="c8298-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="c8298-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8298-102">SYNOPSIS</span></span>
<span data-ttu-id="c8298-103">Annulla la registrazione di un server SCDPM o di un server di backup dal Vault.</span><span class="sxs-lookup"><span data-stu-id="c8298-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8298-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8298-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8298-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8298-105">DESCRIPTION</span></span>
<span data-ttu-id="c8298-106">Il cmdlet **Unregister-AzureRmRecoveryServicesBackupManagementServer** Annulla la registrazione di un server di System Center Data Protection Manager (scdpm) o di un server di backup di Azure dalla volta.</span><span class="sxs-lookup"><span data-stu-id="c8298-106">The **Unregister-AzureRmRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="c8298-107">Questo cmdlet consente di rimuovere i riferimenti ai server di cui è stata annullata la registrazione dal Vault.</span><span class="sxs-lookup"><span data-stu-id="c8298-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>

<span data-ttu-id="c8298-108">Prima di poter annullare la registrazione di un contenitore, è necessario eliminare tutti i dati protetti associati al contenitore.</span><span class="sxs-lookup"><span data-stu-id="c8298-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="c8298-109">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="c8298-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="c8298-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8298-110">EXAMPLES</span></span>

### <span data-ttu-id="c8298-111">Esempio 1: annullare la registrazione di un server SCDPM dal Vault</span><span class="sxs-lookup"><span data-stu-id="c8298-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzureRmRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer $BMS
```

<span data-ttu-id="c8298-112">Il primo comando ottiene il server di gestione di backup denominato dpmserver01.contoso.com e lo archivia nella variabile $BMS.</span><span class="sxs-lookup"><span data-stu-id="c8298-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>

<span data-ttu-id="c8298-113">Il secondo comando Annulla la registrazione del server SCDPM dal Vault.</span><span class="sxs-lookup"><span data-stu-id="c8298-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="c8298-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8298-114">PARAMETERS</span></span>

### <span data-ttu-id="c8298-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="c8298-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="c8298-116">Specifica un oggetto server SCDPM per annullare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="c8298-116">Specifies an SCDPM server object to unregister.</span></span>
<span data-ttu-id="c8298-117">Per ottenere un oggetto **BackupManagementServer** , usa il cmdlet Get-AzureRmRecoveryServicesBackupManagementServer.</span><span class="sxs-lookup"><span data-stu-id="c8298-117">To obtain an **BackupManagementServer** object, use the Get-AzureRmRecoveryServicesBackupManagementServer cmdlet.</span></span>

```yaml
Type: BackupEngineBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8298-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8298-118">-DefaultProfile</span></span>
<span data-ttu-id="c8298-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c8298-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8298-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8298-120">-PassThru</span></span>
<span data-ttu-id="c8298-121">Restituire il server di gestione backup da eliminare.</span><span class="sxs-lookup"><span data-stu-id="c8298-121">Return the Backup Management Server to be deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8298-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c8298-122">-Confirm</span></span>
<span data-ttu-id="c8298-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8298-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8298-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8298-124">-WhatIf</span></span>
<span data-ttu-id="c8298-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8298-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8298-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8298-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8298-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8298-127">CommonParameters</span></span>
<span data-ttu-id="c8298-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8298-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8298-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8298-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8298-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8298-130">INPUTS</span></span>

### <span data-ttu-id="c8298-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c8298-131">None</span></span>
<span data-ttu-id="c8298-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c8298-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c8298-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8298-133">OUTPUTS</span></span>

## <span data-ttu-id="c8298-134">Note</span><span class="sxs-lookup"><span data-stu-id="c8298-134">NOTES</span></span>

## <span data-ttu-id="c8298-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8298-135">RELATED LINKS</span></span>

[<span data-ttu-id="c8298-136">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="c8298-136">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)


