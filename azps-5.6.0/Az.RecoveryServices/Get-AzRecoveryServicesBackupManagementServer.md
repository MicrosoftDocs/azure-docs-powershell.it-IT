---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 50fb3af805adf4e42ab0b6bf1824b09473d98239
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990876"
---
# <span data-ttu-id="9765b-101">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="9765b-101">Get-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="9765b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9765b-102">SYNOPSIS</span></span>
<span data-ttu-id="9765b-103">Recupera SCDPM e i server di gestione del backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="9765b-103">Gets SCDPM and Azure Backup management servers.</span></span>

## <span data-ttu-id="9765b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9765b-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9765b-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9765b-105">DESCRIPTION</span></span>
<span data-ttu-id="9765b-106">Il cmdlet **Get-AzRecoveryServicesBackupManagementServer** ottiene un elenco dei server di gestione del backup registrati in un vault.</span><span class="sxs-lookup"><span data-stu-id="9765b-106">The **Get-AzRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="9765b-107">Esistono due tipi di server di gestione del backup: System Center Data Protection Manager (SCDPM) e i server di gestione di Backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="9765b-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="9765b-108">I server di gestione del backup vengono installati separatamente per gestire la copia di backup.</span><span class="sxs-lookup"><span data-stu-id="9765b-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="9765b-109">Impostare il contesto del vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="9765b-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="9765b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9765b-110">EXAMPLES</span></span>

### <span data-ttu-id="9765b-111">Esempio 1: Ottenere tutti i server di gestione del backup</span><span class="sxs-lookup"><span data-stu-id="9765b-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

<span data-ttu-id="9765b-112">Questo comando recupera tutti i server di gestione del backup registrati con il vault.</span><span class="sxs-lookup"><span data-stu-id="9765b-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="9765b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9765b-113">PARAMETERS</span></span>

### <span data-ttu-id="9765b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9765b-114">-DefaultProfile</span></span>
<span data-ttu-id="9765b-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9765b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9765b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="9765b-116">-Name</span></span>
<span data-ttu-id="9765b-117">Specifica il nome del server di gestione del backup da ottenere.</span><span class="sxs-lookup"><span data-stu-id="9765b-117">Specifies the name of the Backup management server to get.</span></span>

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

### <span data-ttu-id="9765b-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="9765b-118">-VaultId</span></span>
<span data-ttu-id="9765b-119">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9765b-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9765b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9765b-120">CommonParameters</span></span>
<span data-ttu-id="9765b-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9765b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9765b-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9765b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9765b-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="9765b-123">INPUTS</span></span>

### <span data-ttu-id="9765b-124">System.String</span><span class="sxs-lookup"><span data-stu-id="9765b-124">System.String</span></span>

## <span data-ttu-id="9765b-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9765b-125">OUTPUTS</span></span>

### <span data-ttu-id="9765b-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupToolBase</span><span class="sxs-lookup"><span data-stu-id="9765b-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="9765b-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="9765b-127">NOTES</span></span>

## <span data-ttu-id="9765b-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9765b-128">RELATED LINKS</span></span>

[<span data-ttu-id="9765b-129">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="9765b-129">Unregister-AzRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzRecoveryServicesBackupManagementServer.md)


