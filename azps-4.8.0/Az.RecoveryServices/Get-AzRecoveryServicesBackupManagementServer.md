---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 09d27926f489feea397c98a217840bb973e002ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032838"
---
# <span data-ttu-id="5e89b-101">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="5e89b-101">Get-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="5e89b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e89b-102">SYNOPSIS</span></span>
<span data-ttu-id="5e89b-103">Ottiene i server di gestione di SCDPM e Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="5e89b-103">Gets SCDPM and Azure Backup management servers.</span></span>

## <span data-ttu-id="5e89b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e89b-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e89b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e89b-105">DESCRIPTION</span></span>
<span data-ttu-id="5e89b-106">Il cmdlet **Get-AzRecoveryServicesBackupManagementServer** ottiene un elenco dei server di gestione di backup registrati in un Vault.</span><span class="sxs-lookup"><span data-stu-id="5e89b-106">The **Get-AzRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="5e89b-107">Esistono due tipi di server di gestione del backup: System Center Data Protection Manager (SCDPM) e Azure Backup Management Servers.</span><span class="sxs-lookup"><span data-stu-id="5e89b-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="5e89b-108">I server di gestione backup vengono installati separatamente per gestire l'orchestrazione di backup.</span><span class="sxs-lookup"><span data-stu-id="5e89b-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="5e89b-109">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="5e89b-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="5e89b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e89b-110">EXAMPLES</span></span>

### <span data-ttu-id="5e89b-111">Esempio 1: ottenere tutti i server di gestione del backup</span><span class="sxs-lookup"><span data-stu-id="5e89b-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

<span data-ttu-id="5e89b-112">Questo comando consente di ottenere tutti i server di gestione del backup registrati con il Vault.</span><span class="sxs-lookup"><span data-stu-id="5e89b-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="5e89b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e89b-113">PARAMETERS</span></span>

### <span data-ttu-id="5e89b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e89b-114">-DefaultProfile</span></span>
<span data-ttu-id="5e89b-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5e89b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e89b-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5e89b-116">-Name</span></span>
<span data-ttu-id="5e89b-117">Specifica il nome del server di gestione del backup da ottenere.</span><span class="sxs-lookup"><span data-stu-id="5e89b-117">Specifies the name of the Backup management server to get.</span></span>

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

### <span data-ttu-id="5e89b-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="5e89b-118">-VaultId</span></span>
<span data-ttu-id="5e89b-119">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5e89b-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5e89b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e89b-120">CommonParameters</span></span>
<span data-ttu-id="5e89b-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e89b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e89b-122">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e89b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e89b-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e89b-123">INPUTS</span></span>

### <span data-ttu-id="5e89b-124">System. String</span><span class="sxs-lookup"><span data-stu-id="5e89b-124">System.String</span></span>

## <span data-ttu-id="5e89b-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e89b-125">OUTPUTS</span></span>

### <span data-ttu-id="5e89b-126">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="5e89b-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="5e89b-127">Note</span><span class="sxs-lookup"><span data-stu-id="5e89b-127">NOTES</span></span>

## <span data-ttu-id="5e89b-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e89b-128">RELATED LINKS</span></span>

[<span data-ttu-id="5e89b-129">Annullamento della registrazione-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="5e89b-129">Unregister-AzRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzRecoveryServicesBackupManagementServer.md)


