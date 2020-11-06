---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 8A638FB1-F530-4E28-BAAE-5382671092C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupItem.md
ms.openlocfilehash: 892e9385a34f9c02ddcf41d57578bb320d645e0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521937"
---
# <span data-ttu-id="977af-101">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="977af-101">Get-AzureRmBackupItem</span></span>

## <span data-ttu-id="977af-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="977af-102">SYNOPSIS</span></span>
<span data-ttu-id="977af-103">Ottiene gli elementi sotto un contenitore in backup.</span><span class="sxs-lookup"><span data-stu-id="977af-103">Gets the items under a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="977af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="977af-104">SYNTAX</span></span>

```
Get-AzureRmBackupItem [-ProtectionStatus <String>] [-Status <String>] [-Type <String>]
 [-Container] <AzureRMBackupContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="977af-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="977af-105">DESCRIPTION</span></span>
<span data-ttu-id="977af-106">Il cmdlet **Get-AzureRmBackupItem** ottiene gli elementi in un contenitore in Azure Backup e lo stato di protezione degli elementi.</span><span class="sxs-lookup"><span data-stu-id="977af-106">The **Get-AzureRmBackupItem** cmdlet gets the items in a container in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="977af-107">Abilitare gli elementi per la protezione usando il cmdlet Enable-AzureRmBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="977af-107">Enable items for protection by using the Enable-AzureRmBackupProtection cmdlet.</span></span>

<span data-ttu-id="977af-108">Un contenitore registrato in un caveau di backup può avere uno o più elementi che possono essere protetti.</span><span class="sxs-lookup"><span data-stu-id="977af-108">A container that is registered to a Backup vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="977af-109">Per le macchine virtuali di Azure può essere presente un solo elemento nel contenitore della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="977af-109">For Azure virtual machines, there can be only one item in the virtual machine container.</span></span>

## <span data-ttu-id="977af-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="977af-110">EXAMPLES</span></span>

### <span data-ttu-id="977af-111">Esempio 1: recuperare gli elementi in un contenitore</span><span class="sxs-lookup"><span data-stu-id="977af-111">Example 1: Get the items in a container</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type AzureVM -Name "DPMSERVER.CONTOSO.COM"
PS C:\> Get-AzureRmBackupItem -Container $Container
Name                    ProtectionStatus       DataSourceStatus       RecoveryPointsCount    ProtectionPolicyName
----                    ----------------       ----------------       -------------------    --------------------
co03-vm                 NotProtected                                  0
```

<span data-ttu-id="977af-112">Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="977af-112">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="977af-113">Il comando Archivia l'oggetto nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="977af-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="977af-114">Il secondo comando ottiene un contenitore con il nome specificato nel Vault in $Vault usando il cmdlet **Get-AzureRmBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="977af-114">The second command gets a container that has the specified name in the vault in $Vault by using the **Get-AzureRmBackupContainer** cmdlet.</span></span>
<span data-ttu-id="977af-115">Il comando Archivia l'oggetto nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="977af-115">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="977af-116">Il comando finale ottiene l'elemento di backup nel contenitore in $Container.</span><span class="sxs-lookup"><span data-stu-id="977af-116">The final command gets the backup item in the container in $Container.</span></span>

### <span data-ttu-id="977af-117">Esempio 2: visualizzare tutte le proprietà di un elemento</span><span class="sxs-lookup"><span data-stu-id="977af-117">Example 2: View all properties for an item</span></span>
```
PS C:\>Get-AzureRmBackupItem -Container $Container | Select-Object -Property *
Name                 : co03-vm
DataSourceStatus     : 
ProtectionStatus     : NotProtected
Type                 : AzureVM
ProtectionPolicyName : 
ProtectionPolicyId   : 
RecoveryPointsCount  : 0
ItemName             : iaasvmcontainer;co03-vm;co03-vm
ContainerType        : AzureVM
ContainerUniqueName  : iaasvmcontainer;co03-vm;co03-vm
ResourceGroupName    : resourcegroup02
ResourceName         : vault03
Location             : southeastasia
```

<span data-ttu-id="977af-118">Questo comando ottiene l'elemento di backup nel contenitore in $Container e lo passa al cmdlet Select-Object.</span><span class="sxs-lookup"><span data-stu-id="977af-118">This command gets the backup item in the container in $Container, and then passes it to the Select-Object cmdlet.</span></span>
<span data-ttu-id="977af-119">Questo cmdlet restituisce tutte le proprietà dell'elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="977af-119">That cmdlet returns all properties of the backup item.</span></span>
<span data-ttu-id="977af-120">Per altre informazioni, digitare `Get-Help Select-Object` .</span><span class="sxs-lookup"><span data-stu-id="977af-120">For more information, type `Get-Help Select-Object`.</span></span>

## <span data-ttu-id="977af-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="977af-121">PARAMETERS</span></span>

### <span data-ttu-id="977af-122">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="977af-122">-Container</span></span>
<span data-ttu-id="977af-123">Specifica un oggetto contenitore per il quale questo cmdlet ottiene gli elementi di backup.</span><span class="sxs-lookup"><span data-stu-id="977af-123">Specifies a container object for which this cmdlet gets backup items.</span></span>
<span data-ttu-id="977af-124">Per ottenere un **AzureRmBackupContainer** , usare il cmdlet Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="977af-124">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="977af-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="977af-125">-DefaultProfile</span></span>
<span data-ttu-id="977af-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="977af-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="977af-127">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="977af-127">-ProtectionStatus</span></span>
<span data-ttu-id="977af-128">Specifica lo stato di protezione complessivo di un elemento nel contenitore.</span><span class="sxs-lookup"><span data-stu-id="977af-128">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="977af-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="977af-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="977af-130">Protetta</span><span class="sxs-lookup"><span data-stu-id="977af-130">Protected</span></span> 
- <span data-ttu-id="977af-131">Proteggere</span><span class="sxs-lookup"><span data-stu-id="977af-131">Protecting</span></span>  
- <span data-ttu-id="977af-132">NotProtected</span><span class="sxs-lookup"><span data-stu-id="977af-132">NotProtected</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Protected, Protecting, NotProtected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977af-133">-Stato</span><span class="sxs-lookup"><span data-stu-id="977af-133">-Status</span></span>
<span data-ttu-id="977af-134">Specifica lo stato di backup di un elemento.</span><span class="sxs-lookup"><span data-stu-id="977af-134">Specifies the backup status for an item.</span></span>
<span data-ttu-id="977af-135">I valori accettabili per questo parametro sono: IRPending, protected, ProtectionError e ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="977af-135">The acceptable values for this parameter are: IRPending, Protected, ProtectionError, and ProtectionStopped.</span></span>
<span data-ttu-id="977af-136">Se il valore del parametro *ProtectionStatus* è protetto, puoi usare il valore del parametro di *stato* per filtrare gli elementi.</span><span class="sxs-lookup"><span data-stu-id="977af-136">If the *ProtectionStatus* parameter has the value Protected, you can use the *Status* parameter value to filter items.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: IRPending, ProtectionStopped, ProtectionError, Protected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977af-137">-Digitare</span><span class="sxs-lookup"><span data-stu-id="977af-137">-Type</span></span>
<span data-ttu-id="977af-138">Specifica il tipo di elemento ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="977af-138">Specifies the type of item that this cmdlet gets.</span></span>
<span data-ttu-id="977af-139">Attualmente, l'unico valore supportato è AzureVM.</span><span class="sxs-lookup"><span data-stu-id="977af-139">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="977af-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="977af-140">CommonParameters</span></span>
<span data-ttu-id="977af-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="977af-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="977af-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="977af-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="977af-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="977af-143">INPUTS</span></span>

### <span data-ttu-id="977af-144">AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="977af-144">AzureRmBackupContainer</span></span>

## <span data-ttu-id="977af-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="977af-145">OUTPUTS</span></span>

### <span data-ttu-id="977af-146">AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="977af-146">AzureRmBackupItem</span></span>

## <span data-ttu-id="977af-147">Note</span><span class="sxs-lookup"><span data-stu-id="977af-147">NOTES</span></span>

## <span data-ttu-id="977af-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="977af-148">RELATED LINKS</span></span>

[<span data-ttu-id="977af-149">Backup-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="977af-149">Backup-AzureRmBackupItem</span></span>](./Backup-AzureRmBackupItem.md)

[<span data-ttu-id="977af-150">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="977af-150">Disable-AzureRmBackupProtection</span></span>](./Disable-AzureRmBackupProtection.md)

[<span data-ttu-id="977af-151">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="977af-151">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="977af-152">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="977af-152">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="977af-153">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="977af-153">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="977af-154">Ripristinare-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="977af-154">Restore-AzureRmBackupItem</span></span>](./Restore-AzureRmBackupItem.md)


