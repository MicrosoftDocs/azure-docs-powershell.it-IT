---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 1b025825878e2bc97837237e194b0ec37eb298d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520007"
---
# <span data-ttu-id="31833-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="31833-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="31833-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31833-102">SYNOPSIS</span></span>
<span data-ttu-id="31833-103">Annulla la registrazione di un server SCDPM o di un server di backup dal Vault.</span><span class="sxs-lookup"><span data-stu-id="31833-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31833-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31833-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31833-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31833-105">DESCRIPTION</span></span>
<span data-ttu-id="31833-106">Il cmdlet **Unregister-AzureRmRecoveryServicesBackupManagementServer** Annulla la registrazione di un server di System Center Data Protection Manager (scdpm) o di un server di backup di Azure dalla volta.</span><span class="sxs-lookup"><span data-stu-id="31833-106">The **Unregister-AzureRmRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="31833-107">Questo cmdlet consente di rimuovere i riferimenti ai server di cui è stata annullata la registrazione dal Vault.</span><span class="sxs-lookup"><span data-stu-id="31833-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>

<span data-ttu-id="31833-108">Prima di poter annullare la registrazione di un contenitore, è necessario eliminare tutti i dati protetti associati al contenitore.</span><span class="sxs-lookup"><span data-stu-id="31833-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="31833-109">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="31833-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="31833-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31833-110">EXAMPLES</span></span>

### <span data-ttu-id="31833-111">Esempio 1: annullare la registrazione di un server SCDPM dal Vault</span><span class="sxs-lookup"><span data-stu-id="31833-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzureRmRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer $BMS
```

<span data-ttu-id="31833-112">Il primo comando ottiene il server di gestione di backup denominato dpmserver01.contoso.com e lo archivia nella variabile $BMS.</span><span class="sxs-lookup"><span data-stu-id="31833-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>

<span data-ttu-id="31833-113">Il secondo comando Annulla la registrazione del server SCDPM dal Vault.</span><span class="sxs-lookup"><span data-stu-id="31833-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="31833-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31833-114">PARAMETERS</span></span>

### <span data-ttu-id="31833-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="31833-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="31833-116">Specifica un oggetto server SCDPM per annullare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="31833-116">Specifies an SCDPM server object to unregister.</span></span>
<span data-ttu-id="31833-117">Per ottenere un oggetto **BackupManagementServer** , usa il cmdlet Get-AzureRmRecoveryServicesBackupManagementServer.</span><span class="sxs-lookup"><span data-stu-id="31833-117">To obtain an **BackupManagementServer** object, use the Get-AzureRmRecoveryServicesBackupManagementServer cmdlet.</span></span>

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

### <span data-ttu-id="31833-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31833-118">-DefaultProfile</span></span>
<span data-ttu-id="31833-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31833-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31833-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31833-120">CommonParameters</span></span>
<span data-ttu-id="31833-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31833-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31833-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31833-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31833-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31833-123">INPUTS</span></span>

## <span data-ttu-id="31833-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31833-124">OUTPUTS</span></span>

## <span data-ttu-id="31833-125">Note</span><span class="sxs-lookup"><span data-stu-id="31833-125">NOTES</span></span>

## <span data-ttu-id="31833-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31833-126">RELATED LINKS</span></span>

[<span data-ttu-id="31833-127">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="31833-127">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)


