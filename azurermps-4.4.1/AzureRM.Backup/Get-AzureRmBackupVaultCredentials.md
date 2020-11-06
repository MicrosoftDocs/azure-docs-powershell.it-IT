---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9882F1A5-6FFB-4DAF-8ED5-B14596BC939D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
ms.openlocfilehash: b208602532428d14c2af1504c5b8af2cce0b155d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511323"
---
# <span data-ttu-id="b24f4-101">Get-AzureRmBackupVaultCredentials</span><span class="sxs-lookup"><span data-stu-id="b24f4-101">Get-AzureRmBackupVaultCredentials</span></span>

## <span data-ttu-id="b24f4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b24f4-102">SYNOPSIS</span></span>
<span data-ttu-id="b24f4-103">Scarica il file delle credenziali del Vault per un caveau di backup.</span><span class="sxs-lookup"><span data-stu-id="b24f4-103">Downloads the vault credentials file for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b24f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b24f4-104">SYNTAX</span></span>

```
Get-AzureRmBackupVaultCredentials [-TargetLocation] <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b24f4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b24f4-105">DESCRIPTION</span></span>
<span data-ttu-id="b24f4-106">Il cmdlet **Get-AzureRmBackupVaultCredentials** Scarica il file delle credenziali del Vault per un Vault di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="b24f4-106">The **Get-AzureRmBackupVaultCredentials** cmdlet downloads the vault credentials file for an Azure Backup vault.</span></span>

<span data-ttu-id="b24f4-107">Backup usa un file di credenziali del Vault per connettere un server all'archivio di backup di Azure e registrarlo.</span><span class="sxs-lookup"><span data-stu-id="b24f4-107">Backup uses a vault credential file to connect a server to the Azure Backup vault and register it.</span></span>
<span data-ttu-id="b24f4-108">È necessario registrare un server prima che il backup possa inviare dati di backup al Vault.</span><span class="sxs-lookup"><span data-stu-id="b24f4-108">You must register a server before Backup can send backup data to the vault.</span></span>

## <span data-ttu-id="b24f4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b24f4-109">EXAMPLES</span></span>

## <span data-ttu-id="b24f4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b24f4-110">PARAMETERS</span></span>

### <span data-ttu-id="b24f4-111">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="b24f4-111">-TargetLocation</span></span>
<span data-ttu-id="b24f4-112">Specifica il percorso di destinazione in cui questo cmdlet archivia il file delle credenziali del Vault.</span><span class="sxs-lookup"><span data-stu-id="b24f4-112">Specifies the destination path where this cmdlet stores the vault credentials file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b24f4-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="b24f4-113">-Vault</span></span>
<span data-ttu-id="b24f4-114">Specifica il Vault di backup per il quale questo cmdlet ottiene un file di credenziale del Vault.</span><span class="sxs-lookup"><span data-stu-id="b24f4-114">Specifies the Backup vault for which this cmdlet gets a vault credential file.</span></span>
<span data-ttu-id="b24f4-115">Per ottenere un oggetto **AzureRmBackupVault** , usa il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="b24f4-115">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b24f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b24f4-116">-DefaultProfile</span></span>
<span data-ttu-id="b24f4-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b24f4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b24f4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b24f4-118">CommonParameters</span></span>
<span data-ttu-id="b24f4-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b24f4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b24f4-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b24f4-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b24f4-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b24f4-121">INPUTS</span></span>

### <span data-ttu-id="b24f4-122">AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="b24f4-122">AzureRMBackupVault</span></span>

## <span data-ttu-id="b24f4-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b24f4-123">OUTPUTS</span></span>

### <span data-ttu-id="b24f4-124">Stringa</span><span class="sxs-lookup"><span data-stu-id="b24f4-124">String</span></span>
<span data-ttu-id="b24f4-125">Questo cmdlet restituisce il nome del file delle credenziali del Vault.</span><span class="sxs-lookup"><span data-stu-id="b24f4-125">This cmdlet returns the name of the vault credential file.</span></span>

## <span data-ttu-id="b24f4-126">Note</span><span class="sxs-lookup"><span data-stu-id="b24f4-126">NOTES</span></span>

## <span data-ttu-id="b24f4-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b24f4-127">RELATED LINKS</span></span>

[<span data-ttu-id="b24f4-128">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b24f4-128">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


