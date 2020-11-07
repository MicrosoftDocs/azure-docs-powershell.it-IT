---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: DD150A2C-27D5-4119-9B43-FAB82F9F7D5B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/enable-azurermbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Enable-AzureRmBackupProtection.md
ms.openlocfilehash: 87f269042b6d0f660f621a865dda7619afd9be5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687052"
---
# <span data-ttu-id="858b9-101">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="858b9-101">Enable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="858b9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="858b9-102">SYNOPSIS</span></span>
<span data-ttu-id="858b9-103">Associa un elemento a un criterio di protezione di Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="858b9-103">Associates an item with an Azure Backup protection policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="858b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="858b9-104">SYNTAX</span></span>

```
Enable-AzureRmBackupProtection -Policy <AzureRMBackupProtectionPolicy>
 [-Item] <AzureRMBackupContainerContextObject> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="858b9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="858b9-105">DESCRIPTION</span></span>
<span data-ttu-id="858b9-106">Il cmdlet **Enable-AzureRmBackupProtection** associa un elemento a un criterio di protezione di Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="858b9-106">The **Enable-AzureRmBackupProtection** cmdlet associates an item with an Azure Backup protection policy.</span></span>
<span data-ttu-id="858b9-107">Per abilitare un criterio di protezione, è necessario prima avere un elemento di backup esistente e un criterio esistente.</span><span class="sxs-lookup"><span data-stu-id="858b9-107">To enable a protection policy, you must first have an existing backup item and an existing policy.</span></span>
<span data-ttu-id="858b9-108">Entrambi devono appartenere allo stesso caveau di backup.</span><span class="sxs-lookup"><span data-stu-id="858b9-108">Both must belong to the same Backup vault.</span></span>
<span data-ttu-id="858b9-109">La pianificazione del backup esegue la copia iniziale completa per l'elemento e la copia incrementale per i backup successivi.</span><span class="sxs-lookup"><span data-stu-id="858b9-109">The backup schedule does the full initial copy for the item and the incremental copy for the subsequent backups.</span></span>

## <span data-ttu-id="858b9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="858b9-110">EXAMPLES</span></span>

### <span data-ttu-id="858b9-111">Esempio 1: abilitare la protezione in una macchina virtuale di Azure</span><span class="sxs-lookup"><span data-stu-id="858b9-111">Example 1: Enable protection on an Azure virtual machine</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Policy = Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DefaultPolicy"
PS C:\> Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Status Registered | Get-AzureRmBackupItem | Enable-AzureRmBackupProtection -Policy $Policy
WorkloadName    Operation        Status          StartTime              EndTime
------------    ---------        ------          ---------              -------
co03-vm         ConfigureBackup  Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
```

<span data-ttu-id="858b9-112">Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="858b9-112">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="858b9-113">Il comando Archivia l'oggetto nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="858b9-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="858b9-114">Il secondo comando consente di ottenere i criteri di protezione del backup denominati DefaultPolicy per il Vault in $Vault.</span><span class="sxs-lookup"><span data-stu-id="858b9-114">The second command gets the Backup protection policy named DefaultPolicy for the vault in $Vault.</span></span>
<span data-ttu-id="858b9-115">Il comando Archivia l'oggetto nella variabile $Policy.</span><span class="sxs-lookup"><span data-stu-id="858b9-115">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="858b9-116">Il comando finale usa l'operatore pipeline per passare i valori da un cmdlet al successivo.</span><span class="sxs-lookup"><span data-stu-id="858b9-116">The final command uses the pipeline operator to pass values from one cmdlet to the next.</span></span>
<span data-ttu-id="858b9-117">Ottiene un contenitore usando il cmdlet Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="858b9-117">It gets a container, by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="858b9-118">Il comando ottiene l'elemento di backup da tale contenitore usando il cmdlet Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="858b9-118">The command gets the backup item from that container by using the Get-AzureRmBackupItem cmdlet.</span></span>
<span data-ttu-id="858b9-119">Il cmdlet corrente Abilita i criteri archiviati in $Policy per l'elemento che il comando passa al cmdlet.</span><span class="sxs-lookup"><span data-stu-id="858b9-119">The current cmdlet enables the policy stored in $Policy for the item that the command passes to that cmdlet.</span></span>

## <span data-ttu-id="858b9-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="858b9-120">PARAMETERS</span></span>

### <span data-ttu-id="858b9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="858b9-121">-DefaultProfile</span></span>
<span data-ttu-id="858b9-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="858b9-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="858b9-123">-Elemento</span><span class="sxs-lookup"><span data-stu-id="858b9-123">-Item</span></span>
<span data-ttu-id="858b9-124">Specifica l'elemento di backup per cui questo cmdlet Abilita la protezione.</span><span class="sxs-lookup"><span data-stu-id="858b9-124">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="858b9-125">Per ottenere un **AzureRmBackupItem** , usare il cmdlet Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="858b9-125">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: AzureRMBackupContainerContextObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="858b9-126">-Policy</span><span class="sxs-lookup"><span data-stu-id="858b9-126">-Policy</span></span>
<span data-ttu-id="858b9-127">Specifica i criteri di protezione che il cmdlet associa a un elemento.</span><span class="sxs-lookup"><span data-stu-id="858b9-127">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="858b9-128">Per ottenere un oggetto **AzureRmBackupProtectionPolicy** , usa il cmdlet Get-AzureRmBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="858b9-128">To obtain an **AzureRmBackupProtectionPolicy** object, use the Get-AzureRmBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="858b9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="858b9-129">CommonParameters</span></span>
<span data-ttu-id="858b9-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="858b9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="858b9-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="858b9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="858b9-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="858b9-132">INPUTS</span></span>

### <span data-ttu-id="858b9-133">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="858b9-133">AzureRmBackupItem</span></span>

## <span data-ttu-id="858b9-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="858b9-134">OUTPUTS</span></span>

### <span data-ttu-id="858b9-135">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="858b9-135">AzureRmBackupJob</span></span>

## <span data-ttu-id="858b9-136">Note</span><span class="sxs-lookup"><span data-stu-id="858b9-136">NOTES</span></span>

## <span data-ttu-id="858b9-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="858b9-137">RELATED LINKS</span></span>

[<span data-ttu-id="858b9-138">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="858b9-138">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="858b9-139">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="858b9-139">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)

[<span data-ttu-id="858b9-140">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="858b9-140">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)


