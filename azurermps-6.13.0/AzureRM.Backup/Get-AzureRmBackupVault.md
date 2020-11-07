---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: c11170e6bee80b9eaa19135ad604d8bf70e1baab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686937"
---
# <span data-ttu-id="b3424-101">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b3424-101">Get-AzureRmBackupVault</span></span>

## <span data-ttu-id="b3424-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3424-102">SYNOPSIS</span></span>
<span data-ttu-id="b3424-103">Ottiene i Vault di backup.</span><span class="sxs-lookup"><span data-stu-id="b3424-103">Gets Backup vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3424-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3424-104">SYNTAX</span></span>

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3424-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3424-105">DESCRIPTION</span></span>
<span data-ttu-id="b3424-106">Il cmdlet **Get-AzureRmBackupVault** ottiene i Vault di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="b3424-106">The **Get-AzureRmBackupVault** cmdlet gets Azure Backup vaults.</span></span>
<span data-ttu-id="b3424-107">Questo cmdlet restituisce gli oggetti **AzureRmBackupVault** da usare con altri cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3424-107">This cmdlet returns **AzureRmBackupVault** objects for use with other cmdlets.</span></span>

## <span data-ttu-id="b3424-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3424-108">EXAMPLES</span></span>

### <span data-ttu-id="b3424-109">Esempio 1: visualizzare tutti i Vault di backup</span><span class="sxs-lookup"><span data-stu-id="b3424-109">Example 1: View all the Backup vaults</span></span>
```
PS C:\>Get-AzureRmBackupVault
```

<span data-ttu-id="b3424-110">Questo comando consente di ottenere tutte le volte di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="b3424-110">This command gets all the Azure Backup vaults.</span></span>

### <span data-ttu-id="b3424-111">Esempio 2: visualizzare tutti i Vault creati in West US</span><span class="sxs-lookup"><span data-stu-id="b3424-111">Example 2: View all vaults created in West US</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

<span data-ttu-id="b3424-112">Questo comando recupera tutti i caveau di backup.</span><span class="sxs-lookup"><span data-stu-id="b3424-112">This command gets all the Backup vaults.</span></span>
<span data-ttu-id="b3424-113">Il comando li passa al cmdlet Where-Object usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="b3424-113">The command passes them to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b3424-114">Questo cmdlet filtra i risultati in base alla proprietà **Region** .</span><span class="sxs-lookup"><span data-stu-id="b3424-114">That cmdlet filters the results based on the **Region** property.</span></span>
<span data-ttu-id="b3424-115">Per altre informazioni, digitare `Get-Help Where-Object` .</span><span class="sxs-lookup"><span data-stu-id="b3424-115">For more information, type `Get-Help Where-Object`.</span></span>

### <span data-ttu-id="b3424-116">Esempio 3: ottenere un Vault specifico</span><span class="sxs-lookup"><span data-stu-id="b3424-116">Example 3: Get a specific vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="b3424-117">Questo comando ottiene il Vault denominato Vault03.</span><span class="sxs-lookup"><span data-stu-id="b3424-117">This command gets the vault named Vault03.</span></span>

### <span data-ttu-id="b3424-118">Esempio 4: contare il numero di volte con spazio di archiviazione locale ridondante</span><span class="sxs-lookup"><span data-stu-id="b3424-118">Example 4: Count the number of vaults that have locally redundant storage</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

<span data-ttu-id="b3424-119">Questo comando consente di ottenere tutte le volte di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="b3424-119">This command gets all the Azure Backup vaults.</span></span>
<span data-ttu-id="b3424-120">Il comando li passa a **Where-Object** , che filtra i risultati in base alla proprietà di **archiviazione** .</span><span class="sxs-lookup"><span data-stu-id="b3424-120">The command passes them to **Where-Object** , which filters the results based on the **Storage** property.</span></span>
<span data-ttu-id="b3424-121">Il comando passa quelli che hanno un valore di LocallyRedundant al cmdlet Measure-Object, che conteggia i risultati.</span><span class="sxs-lookup"><span data-stu-id="b3424-121">The command passes the ones that have a value of LocallyRedundant to the Measure-Object cmdlet, which counts the results.</span></span>
<span data-ttu-id="b3424-122">Per altre informazioni, digitare `Get-Help Measure-Object` .</span><span class="sxs-lookup"><span data-stu-id="b3424-122">For more information, type `Get-Help Measure-Object`.</span></span>

## <span data-ttu-id="b3424-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3424-123">PARAMETERS</span></span>

### <span data-ttu-id="b3424-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3424-124">-DefaultProfile</span></span>
<span data-ttu-id="b3424-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b3424-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3424-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3424-126">-Name</span></span>
<span data-ttu-id="b3424-127">Specifica il nome dell'archivio di backup ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3424-127">Specifies the name of the Backup vault that this cmdlet gets.</span></span>
<span data-ttu-id="b3424-128">Se più di un Vault di backup ha lo stesso nome, questo cmdlet li restituirà tutti.</span><span class="sxs-lookup"><span data-stu-id="b3424-128">If more than one Backup vault has the same name, this cmdlet returns them all.</span></span>
<span data-ttu-id="b3424-129">Specifica il parametro *ResourceGroupName* per ottenere un Vault univoco.</span><span class="sxs-lookup"><span data-stu-id="b3424-129">Specify the *ResourceGroupName* parameter to get a unique vault.</span></span>

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

### <span data-ttu-id="b3424-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3424-130">-ResourceGroupName</span></span>
<span data-ttu-id="b3424-131">Specifica il nome di un gruppo di risorse Azure in cui questo cmdlet ottiene un caveau di backup.</span><span class="sxs-lookup"><span data-stu-id="b3424-131">Specifies the name of an Azure resource group in which this cmdlet gets a Backup vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3424-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3424-132">CommonParameters</span></span>
<span data-ttu-id="b3424-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3424-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3424-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3424-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3424-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3424-135">INPUTS</span></span>

### <span data-ttu-id="b3424-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b3424-136">None</span></span>

## <span data-ttu-id="b3424-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3424-137">OUTPUTS</span></span>

### <span data-ttu-id="b3424-138">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="b3424-138">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>

## <span data-ttu-id="b3424-139">Note</span><span class="sxs-lookup"><span data-stu-id="b3424-139">NOTES</span></span>

## <span data-ttu-id="b3424-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3424-140">RELATED LINKS</span></span>

[<span data-ttu-id="b3424-141">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b3424-141">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="b3424-142">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b3424-142">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="b3424-143">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b3424-143">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="b3424-144">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="b3424-144">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


