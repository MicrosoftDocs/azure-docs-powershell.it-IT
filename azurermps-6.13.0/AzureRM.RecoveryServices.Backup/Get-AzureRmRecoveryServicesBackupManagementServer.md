---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: c3419f020aca0853d94d8848e944e39fc8ed05a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514927"
---
# <span data-ttu-id="0c5ef-101">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="0c5ef-101">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="0c5ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c5ef-102">SYNOPSIS</span></span>
<span data-ttu-id="0c5ef-103">Ottiene i server di gestione di SCDPM e Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="0c5ef-103">Gets SCDPM and Azure Backup management servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c5ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c5ef-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c5ef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c5ef-105">DESCRIPTION</span></span>
<span data-ttu-id="0c5ef-106">Il cmdlet **Get-AzureRmRecoveryServicesBackupManagementServer** ottiene un elenco dei server di gestione di backup registrati in un Vault.</span><span class="sxs-lookup"><span data-stu-id="0c5ef-106">The **Get-AzureRmRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="0c5ef-107">Esistono due tipi di server di gestione del backup: System Center Data Protection Manager (SCDPM) e Azure Backup Management Servers.</span><span class="sxs-lookup"><span data-stu-id="0c5ef-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="0c5ef-108">I server di gestione backup vengono installati separatamente per gestire l'orchestrazione di backup.</span><span class="sxs-lookup"><span data-stu-id="0c5ef-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="0c5ef-109">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="0c5ef-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="0c5ef-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c5ef-110">EXAMPLES</span></span>

### <span data-ttu-id="0c5ef-111">Esempio 1: ottenere tutti i server di gestione del backup</span><span class="sxs-lookup"><span data-stu-id="0c5ef-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupManagementServer
```

<span data-ttu-id="0c5ef-112">Questo comando consente di ottenere tutti i server di gestione del backup registrati con il Vault.</span><span class="sxs-lookup"><span data-stu-id="0c5ef-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="0c5ef-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c5ef-113">PARAMETERS</span></span>

### <span data-ttu-id="0c5ef-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c5ef-114">-DefaultProfile</span></span>
<span data-ttu-id="0c5ef-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c5ef-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c5ef-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="0c5ef-116">-Name</span></span>
<span data-ttu-id="0c5ef-117">Specifica il nome del server di gestione del backup da ottenere.</span><span class="sxs-lookup"><span data-stu-id="0c5ef-117">Specifies the name of the Backup management server to get.</span></span>

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

### <span data-ttu-id="0c5ef-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0c5ef-118">-VaultId</span></span>
<span data-ttu-id="0c5ef-119">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="0c5ef-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0c5ef-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c5ef-120">CommonParameters</span></span>
<span data-ttu-id="0c5ef-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c5ef-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c5ef-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c5ef-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c5ef-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c5ef-123">INPUTS</span></span>

### <span data-ttu-id="0c5ef-124">System. String</span><span class="sxs-lookup"><span data-stu-id="0c5ef-124">System.String</span></span>
<span data-ttu-id="0c5ef-125">Parametri: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0c5ef-125">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="0c5ef-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c5ef-126">OUTPUTS</span></span>

### <span data-ttu-id="0c5ef-127">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="0c5ef-127">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="0c5ef-128">Note</span><span class="sxs-lookup"><span data-stu-id="0c5ef-128">NOTES</span></span>

## <span data-ttu-id="0c5ef-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c5ef-129">RELATED LINKS</span></span>

[<span data-ttu-id="0c5ef-130">Annullamento della registrazione-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="0c5ef-130">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzureRmRecoveryServicesBackupManagementServer.md)


