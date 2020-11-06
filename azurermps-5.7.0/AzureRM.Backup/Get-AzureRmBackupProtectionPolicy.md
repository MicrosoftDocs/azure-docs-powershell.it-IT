---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: B3B708C5-776E-4F1C-BA0B-492CD9057794
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: d0f0e52db76f4f16f41d1758b7e568ee17d6eede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512735"
---
# <span data-ttu-id="169ce-101">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="169ce-101">Get-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="169ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="169ce-102">SYNOPSIS</span></span>
<span data-ttu-id="169ce-103">Ottiene i criteri di backup per un Vault di backup.</span><span class="sxs-lookup"><span data-stu-id="169ce-103">Gets backup policies for a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="169ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="169ce-104">SYNTAX</span></span>

```
Get-AzureRmBackupProtectionPolicy [[-Name] <String>] [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="169ce-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="169ce-105">DESCRIPTION</span></span>
<span data-ttu-id="169ce-106">Il cmdlet **Get-AzureRmBackupProtectionPolicy** ottiene i criteri di backup per un Vault di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="169ce-106">The **Get-AzureRmBackupProtectionPolicy** cmdlet gets backup policies for an Azure Backup vault.</span></span>

## <span data-ttu-id="169ce-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="169ce-107">EXAMPLES</span></span>

### <span data-ttu-id="169ce-108">Esempio 1: visualizzare i criteri in un Vault</span><span class="sxs-lookup"><span data-stu-id="169ce-108">Example 1: View the policies in a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault 
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
contoso01                 AzureVM            Daily              26-Aug-15 3:00:00 PM
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
DefaultPolicy             AzureVM            Daily              26-Aug-15 12:30:00 AM
WeeklyBkp                 AzureVM            Weekly             26-Aug-15 5:00:00 PM
contoso02                 AzureVM            Daily              26-Aug-15 3:00:00 PM
```

<span data-ttu-id="169ce-109">Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="169ce-109">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="169ce-110">Il comando Archivia l'oggetto nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="169ce-110">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="169ce-111">Il secondo comando ottiene tutti i criteri di protezione del backup per il Vault in $Vault.</span><span class="sxs-lookup"><span data-stu-id="169ce-111">The second command gets all the Backup protection policies for the vault in $Vault.</span></span>

### <span data-ttu-id="169ce-112">Esempio 2: ottenere un criterio specifico da un Vault</span><span class="sxs-lookup"><span data-stu-id="169ce-112">Example 2: Get a specific policy from a vault</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DefaultPolicy             AzureVM            Daily              26-Aug-15 12:30:00 AM
```

<span data-ttu-id="169ce-113">Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="169ce-113">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="169ce-114">Il comando Archivia l'oggetto nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="169ce-114">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="169ce-115">Il secondo comando consente di ottenere i criteri di protezione del backup denominati DefaultPolicy per il Vault in $Vault.</span><span class="sxs-lookup"><span data-stu-id="169ce-115">The second command gets the Backup protection policy named DefaultPolicy for the vault in $Vault.</span></span>

## <span data-ttu-id="169ce-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="169ce-116">PARAMETERS</span></span>

### <span data-ttu-id="169ce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="169ce-117">-DefaultProfile</span></span>
<span data-ttu-id="169ce-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="169ce-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="169ce-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="169ce-119">-Name</span></span>
<span data-ttu-id="169ce-120">Specifica il nome del criterio ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="169ce-120">Specifies the name of the policy that this cmdlet gets.</span></span>

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

### <span data-ttu-id="169ce-121">-Vault</span><span class="sxs-lookup"><span data-stu-id="169ce-121">-Vault</span></span>
<span data-ttu-id="169ce-122">Specifica il Vault di backup per cui questo cmdlet ottiene i criteri.</span><span class="sxs-lookup"><span data-stu-id="169ce-122">Specifies the Backup vault for which this cmdlet gets policies.</span></span>
<span data-ttu-id="169ce-123">Per ottenere un oggetto **AzureRmBackupVault** , usa il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="169ce-123">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="169ce-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="169ce-124">CommonParameters</span></span>
<span data-ttu-id="169ce-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="169ce-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="169ce-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="169ce-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="169ce-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="169ce-127">INPUTS</span></span>

### <span data-ttu-id="169ce-128">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="169ce-128">AzureRmBackupVault</span></span>

## <span data-ttu-id="169ce-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="169ce-129">OUTPUTS</span></span>

### <span data-ttu-id="169ce-130">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="169ce-130">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="169ce-131">Note</span><span class="sxs-lookup"><span data-stu-id="169ce-131">NOTES</span></span>
* <span data-ttu-id="169ce-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="169ce-132">None</span></span>

## <span data-ttu-id="169ce-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="169ce-133">RELATED LINKS</span></span>

[<span data-ttu-id="169ce-134">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="169ce-134">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="169ce-135">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="169ce-135">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="169ce-136">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="169ce-136">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="169ce-137">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="169ce-137">Remove-AzureRmBackupProtectionPolicy</span></span>](./Remove-AzureRmBackupProtectionPolicy.md)

