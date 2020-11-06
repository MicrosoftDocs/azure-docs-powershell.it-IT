---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: D57C32D1-EB4F-495E-A11B-3B4066E8C552
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/set-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Set-AzureRmBackupVault.md
ms.openlocfilehash: edb119484d397241b786ff9476b688e150ed3c6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511947"
---
# <span data-ttu-id="3fd44-101">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="3fd44-101">Set-AzureRmBackupVault</span></span>

## <span data-ttu-id="3fd44-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3fd44-102">SYNOPSIS</span></span>
<span data-ttu-id="3fd44-103">Modifica il tipo di archiviazione di un caveau di backup.</span><span class="sxs-lookup"><span data-stu-id="3fd44-103">Changes the storage type of a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fd44-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3fd44-104">SYNTAX</span></span>

```
Set-AzureRmBackupVault [[-Storage] <AzureBackupVaultStorageType>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3fd44-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3fd44-105">DESCRIPTION</span></span>
<span data-ttu-id="3fd44-106">Il cmdlet **set-AzureRmBackupVault** modifica il tipo di archiviazione di un Vault di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="3fd44-106">The **Set-AzureRmBackupVault** cmdlet changes the storage type of an Azure Backup vault.</span></span>
<span data-ttu-id="3fd44-107">Non è possibile modificare altre proprietà di un Vault.</span><span class="sxs-lookup"><span data-stu-id="3fd44-107">You cannot modify other properties of a vault.</span></span>

## <span data-ttu-id="3fd44-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3fd44-108">EXAMPLES</span></span>

### <span data-ttu-id="3fd44-109">Esempio 1: cambiare lo spazio di archiviazione per un vault esistente</span><span class="sxs-lookup"><span data-stu-id="3fd44-109">Example 1: Change the storage for an existing vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Set-AzureRmBackupVault -Storage LocallyRedundant
```

<span data-ttu-id="3fd44-110">Questo comando ottiene il Vault di backup di Azure denominato Vault03 usando il cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="3fd44-110">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="3fd44-111">Il comando passa il Vault al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="3fd44-111">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3fd44-112">Il cmdlet corrente modifica il tipo di archiviazione in LocallyRedundant.</span><span class="sxs-lookup"><span data-stu-id="3fd44-112">The current cmdlet changes the storage type to LocallyRedundant.</span></span>

## <span data-ttu-id="3fd44-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3fd44-113">PARAMETERS</span></span>

### <span data-ttu-id="3fd44-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fd44-114">-DefaultProfile</span></span>
<span data-ttu-id="3fd44-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3fd44-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fd44-116">-Spazio di archiviazione</span><span class="sxs-lookup"><span data-stu-id="3fd44-116">-Storage</span></span>
<span data-ttu-id="3fd44-117">Specifica il tipo di archiviazione per i dati di backup.</span><span class="sxs-lookup"><span data-stu-id="3fd44-117">Specifies the storage type for the backup data.</span></span>
<span data-ttu-id="3fd44-118">I valori accettabili per questo parametro sono: LocallyRedundant e georidondanti.</span><span class="sxs-lookup"><span data-stu-id="3fd44-118">The acceptable values for this parameter are: LocallyRedundant and GeoRedundant.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureBackupVaultStorageType
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd44-119">-Vault</span><span class="sxs-lookup"><span data-stu-id="3fd44-119">-Vault</span></span>
<span data-ttu-id="3fd44-120">Specifica un archivio di backup modificato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fd44-120">Specifies a Backup vault that this cmdlet modifies.</span></span>
<span data-ttu-id="3fd44-121">Per ottenere un oggetto **AzureRmBackupVault** , usa il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="3fd44-121">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="3fd44-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fd44-122">CommonParameters</span></span>
<span data-ttu-id="3fd44-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fd44-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fd44-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fd44-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fd44-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3fd44-125">INPUTS</span></span>

### <span data-ttu-id="3fd44-126">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="3fd44-126">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="3fd44-127">Parameters: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3fd44-127">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="3fd44-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3fd44-128">OUTPUTS</span></span>

### <span data-ttu-id="3fd44-129">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="3fd44-129">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>

## <span data-ttu-id="3fd44-130">Note</span><span class="sxs-lookup"><span data-stu-id="3fd44-130">NOTES</span></span>
* <span data-ttu-id="3fd44-131">Quando si registra il primo server o una macchina virtuale per un Vault, il tipo di archiviazione è bloccato.</span><span class="sxs-lookup"><span data-stu-id="3fd44-131">When you register the first server or virtual machine for a vault, the storage type is locked.</span></span> <span data-ttu-id="3fd44-132">In seguito, non è possibile modificare il tipo di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3fd44-132">Subsequently, you cannot change the storage type.</span></span>

## <span data-ttu-id="3fd44-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3fd44-133">RELATED LINKS</span></span>

[<span data-ttu-id="3fd44-134">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="3fd44-134">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="3fd44-135">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="3fd44-135">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="3fd44-136">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="3fd44-136">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)


