---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 341b222c8b5e85a4b5f5221c34d6f45cd2993c71
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677661"
---
# <span data-ttu-id="7c508-101">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="7c508-101">Get-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="7c508-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c508-102">SYNOPSIS</span></span>
<span data-ttu-id="7c508-103">Ottiene i server di gestione di SCDPM e Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="7c508-103">Gets SCDPM and Azure Backup management servers.</span></span>

## <span data-ttu-id="7c508-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c508-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c508-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c508-105">DESCRIPTION</span></span>
<span data-ttu-id="7c508-106">Il cmdlet **Get-AzRecoveryServicesBackupManagementServer** ottiene un elenco dei server di gestione di backup registrati in un Vault.</span><span class="sxs-lookup"><span data-stu-id="7c508-106">The **Get-AzRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="7c508-107">Esistono due tipi di server di gestione del backup: System Center Data Protection Manager (SCDPM) e Azure Backup Management Servers.</span><span class="sxs-lookup"><span data-stu-id="7c508-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="7c508-108">I server di gestione backup vengono installati separatamente per gestire l'orchestrazione di backup.</span><span class="sxs-lookup"><span data-stu-id="7c508-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="7c508-109">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="7c508-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="7c508-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c508-110">EXAMPLES</span></span>

### <span data-ttu-id="7c508-111">Esempio 1: ottenere tutti i server di gestione del backup</span><span class="sxs-lookup"><span data-stu-id="7c508-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

<span data-ttu-id="7c508-112">Questo comando consente di ottenere tutti i server di gestione del backup registrati con il Vault.</span><span class="sxs-lookup"><span data-stu-id="7c508-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="7c508-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c508-113">PARAMETERS</span></span>

### <span data-ttu-id="7c508-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c508-114">-DefaultProfile</span></span>
<span data-ttu-id="7c508-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c508-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c508-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c508-116">-Name</span></span>
<span data-ttu-id="7c508-117">Specifica il nome del server di gestione del backup da ottenere.</span><span class="sxs-lookup"><span data-stu-id="7c508-117">Specifies the name of the Backup management server to get.</span></span>

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

### <span data-ttu-id="7c508-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7c508-118">-VaultId</span></span>
<span data-ttu-id="7c508-119">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7c508-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="7c508-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c508-120">CommonParameters</span></span>
<span data-ttu-id="7c508-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c508-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c508-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c508-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c508-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c508-123">INPUTS</span></span>

### <span data-ttu-id="7c508-124">System. String</span><span class="sxs-lookup"><span data-stu-id="7c508-124">System.String</span></span>

## <span data-ttu-id="7c508-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c508-125">OUTPUTS</span></span>

### <span data-ttu-id="7c508-126">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="7c508-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="7c508-127">Note</span><span class="sxs-lookup"><span data-stu-id="7c508-127">NOTES</span></span>

## <span data-ttu-id="7c508-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c508-128">RELATED LINKS</span></span>

[<span data-ttu-id="7c508-129">Annullamento della registrazione-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="7c508-129">Unregister-AzRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzRecoveryServicesBackupManagementServer.md)


