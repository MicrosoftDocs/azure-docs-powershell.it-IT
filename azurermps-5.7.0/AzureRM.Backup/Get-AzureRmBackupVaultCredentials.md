---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 9882F1A5-6FFB-4DAF-8ED5-B14596BC939D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvaultcredentials
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVaultCredentials.md
ms.openlocfilehash: e6e56b1b9026aa0bba4442edc9652372505983ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687049"
---
# <span data-ttu-id="6d9b0-101">Get-AzureRmBackupVaultCredentials</span><span class="sxs-lookup"><span data-stu-id="6d9b0-101">Get-AzureRmBackupVaultCredentials</span></span>

## <span data-ttu-id="6d9b0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6d9b0-102">SYNOPSIS</span></span>
<span data-ttu-id="6d9b0-103">Scarica il file delle credenziali del Vault per un caveau di backup.</span><span class="sxs-lookup"><span data-stu-id="6d9b0-103">Downloads the vault credentials file for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d9b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d9b0-104">SYNTAX</span></span>

```
Get-AzureRmBackupVaultCredentials [-TargetLocation] <String> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d9b0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6d9b0-105">DESCRIPTION</span></span>
<span data-ttu-id="6d9b0-106">Il cmdlet **Get-AzureRmBackupVaultCredentials** Scarica il file delle credenziali del Vault per un Vault di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="6d9b0-106">The **Get-AzureRmBackupVaultCredentials** cmdlet downloads the vault credentials file for an Azure Backup vault.</span></span>

<span data-ttu-id="6d9b0-107">Backup usa un file di credenziali del Vault per connettere un server all'archivio di backup di Azure e registrarlo.</span><span class="sxs-lookup"><span data-stu-id="6d9b0-107">Backup uses a vault credential file to connect a server to the Azure Backup vault and register it.</span></span>
<span data-ttu-id="6d9b0-108">È necessario registrare un server prima che il backup possa inviare dati di backup al Vault.</span><span class="sxs-lookup"><span data-stu-id="6d9b0-108">You must register a server before Backup can send backup data to the vault.</span></span>

## <span data-ttu-id="6d9b0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d9b0-109">EXAMPLES</span></span>

## <span data-ttu-id="6d9b0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6d9b0-110">PARAMETERS</span></span>

### <span data-ttu-id="6d9b0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d9b0-111">-DefaultProfile</span></span>
<span data-ttu-id="6d9b0-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6d9b0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d9b0-113">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="6d9b0-113">-TargetLocation</span></span>
<span data-ttu-id="6d9b0-114">Specifica il percorso di destinazione in cui questo cmdlet archivia il file delle credenziali del Vault.</span><span class="sxs-lookup"><span data-stu-id="6d9b0-114">Specifies the destination path where this cmdlet stores the vault credentials file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d9b0-115">-Vault</span><span class="sxs-lookup"><span data-stu-id="6d9b0-115">-Vault</span></span>
<span data-ttu-id="6d9b0-116">Specifica il Vault di backup per il quale questo cmdlet ottiene un file di credenziale del Vault.</span><span class="sxs-lookup"><span data-stu-id="6d9b0-116">Specifies the Backup vault for which this cmdlet gets a vault credential file.</span></span>
<span data-ttu-id="6d9b0-117">Per ottenere un oggetto **AzureRmBackupVault** , usa il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="6d9b0-117">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d9b0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d9b0-118">CommonParameters</span></span>
<span data-ttu-id="6d9b0-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d9b0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d9b0-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d9b0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d9b0-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6d9b0-121">INPUTS</span></span>

### <span data-ttu-id="6d9b0-122">AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="6d9b0-122">AzureRMBackupVault</span></span>

## <span data-ttu-id="6d9b0-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d9b0-123">OUTPUTS</span></span>

### <span data-ttu-id="6d9b0-124">Stringa</span><span class="sxs-lookup"><span data-stu-id="6d9b0-124">String</span></span>
<span data-ttu-id="6d9b0-125">Questo cmdlet restituisce il nome del file delle credenziali del Vault.</span><span class="sxs-lookup"><span data-stu-id="6d9b0-125">This cmdlet returns the name of the vault credential file.</span></span>

## <span data-ttu-id="6d9b0-126">Note</span><span class="sxs-lookup"><span data-stu-id="6d9b0-126">NOTES</span></span>

## <span data-ttu-id="6d9b0-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d9b0-127">RELATED LINKS</span></span>

[<span data-ttu-id="6d9b0-128">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="6d9b0-128">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)


