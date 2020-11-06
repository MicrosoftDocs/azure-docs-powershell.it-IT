---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 0dac27b7e17a9336db198906cdfb60fb15738795
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509748"
---
# <span data-ttu-id="b73d4-101">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="b73d4-101">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="b73d4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b73d4-102">SYNOPSIS</span></span>
<span data-ttu-id="b73d4-103">Ottiene i server di gestione di SCDPM e Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="b73d4-103">Gets SCDPM and Azure Backup management servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b73d4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b73d4-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupManagementServer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b73d4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b73d4-105">DESCRIPTION</span></span>
<span data-ttu-id="b73d4-106">Il cmdlet **Get-AzureRmRecoveryServicesBackupManagementServer** ottiene un elenco dei server di gestione di backup registrati in un Vault.</span><span class="sxs-lookup"><span data-stu-id="b73d4-106">The **Get-AzureRmRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>

<span data-ttu-id="b73d4-107">Esistono due tipi di server di gestione del backup: System Center Data Protection Manager (SCDPM) e Azure Backup Management Servers.</span><span class="sxs-lookup"><span data-stu-id="b73d4-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="b73d4-108">I server di gestione backup vengono installati separatamente per gestire l'orchestrazione di backup.</span><span class="sxs-lookup"><span data-stu-id="b73d4-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>

<span data-ttu-id="b73d4-109">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="b73d4-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="b73d4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b73d4-110">EXAMPLES</span></span>

### <span data-ttu-id="b73d4-111">Esempio 1: ottenere tutti i server di gestione del backup</span><span class="sxs-lookup"><span data-stu-id="b73d4-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupManagementServer
```

<span data-ttu-id="b73d4-112">Questo comando consente di ottenere tutti i server di gestione del backup registrati con il Vault.</span><span class="sxs-lookup"><span data-stu-id="b73d4-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="b73d4-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b73d4-113">PARAMETERS</span></span>

### <span data-ttu-id="b73d4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b73d4-114">-DefaultProfile</span></span>
<span data-ttu-id="b73d4-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b73d4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b73d4-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="b73d4-116">-Name</span></span>
<span data-ttu-id="b73d4-117">Specifica il nome del server di gestione del backup da ottenere.</span><span class="sxs-lookup"><span data-stu-id="b73d4-117">Specifies the name of the Backup management server to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b73d4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b73d4-118">CommonParameters</span></span>
<span data-ttu-id="b73d4-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b73d4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b73d4-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b73d4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b73d4-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b73d4-121">INPUTS</span></span>

### <span data-ttu-id="b73d4-122">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b73d4-122">None</span></span>
<span data-ttu-id="b73d4-123">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="b73d4-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b73d4-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b73d4-124">OUTPUTS</span></span>

### <span data-ttu-id="b73d4-125">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="b73d4-125">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

### <span data-ttu-id="b73d4-126">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. BackupEngineBase]</span><span class="sxs-lookup"><span data-stu-id="b73d4-126">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase]</span></span>

## <span data-ttu-id="b73d4-127">Note</span><span class="sxs-lookup"><span data-stu-id="b73d4-127">NOTES</span></span>

## <span data-ttu-id="b73d4-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b73d4-128">RELATED LINKS</span></span>

[<span data-ttu-id="b73d4-129">Annullamento della registrazione-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="b73d4-129">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzureRmRecoveryServicesBackupManagementServer.md)


