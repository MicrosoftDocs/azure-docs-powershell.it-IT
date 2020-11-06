---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6E886340-864C-4FF6-8FA3-669D637770F3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/disable-azurermbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
ms.openlocfilehash: ebea82628aae6df23d16a341f3fd503870a8037a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520285"
---
# <span data-ttu-id="563df-101">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="563df-101">Disable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="563df-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="563df-102">SYNOPSIS</span></span>
<span data-ttu-id="563df-103">Disabilita la protezione per un elemento protetto di backup.</span><span class="sxs-lookup"><span data-stu-id="563df-103">Disables protection for a Backup protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="563df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="563df-104">SYNTAX</span></span>

```
Disable-AzureRmBackupProtection [-RemoveRecoveryPoints] [-Force] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="563df-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="563df-105">DESCRIPTION</span></span>
<span data-ttu-id="563df-106">Il cmdlet **Disable-AzureRmBackupProtection Disabilita** la protezione per un elemento protetto di Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="563df-106">The **Disable-AzureRmBackupProtection** cmdlet disables protection for an Azure Backup protected item.</span></span>
<span data-ttu-id="563df-107">Questo cmdlet interrompe il backup pianificato regolare di un elemento.</span><span class="sxs-lookup"><span data-stu-id="563df-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="563df-108">Questo cmdlet può eliminare i punti di ripristino esistenti per l'elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="563df-108">This cmdlet can delete existing recovery points for the backup item.</span></span>

## <span data-ttu-id="563df-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="563df-109">EXAMPLES</span></span>

## <span data-ttu-id="563df-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="563df-110">PARAMETERS</span></span>

### <span data-ttu-id="563df-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="563df-111">-DefaultProfile</span></span>
<span data-ttu-id="563df-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="563df-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="563df-113">-Force</span><span class="sxs-lookup"><span data-stu-id="563df-113">-Force</span></span>
<span data-ttu-id="563df-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="563df-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="563df-115">-Elemento</span><span class="sxs-lookup"><span data-stu-id="563df-115">-Item</span></span>
<span data-ttu-id="563df-116">Specifica l'elemento di backup per cui questo cmdlet disabilita la protezione.</span><span class="sxs-lookup"><span data-stu-id="563df-116">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="563df-117">Per ottenere un **AzureRmBackupItem** , usare il cmdlet Get-AzureRmBackupItem.</span><span class="sxs-lookup"><span data-stu-id="563df-117">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="563df-118">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="563df-118">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="563df-119">Indica che questo cmdlet elimina i punti di ripristino esistenti.</span><span class="sxs-lookup"><span data-stu-id="563df-119">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="563df-120">Per eliminare i punti di ripristino archiviati in un secondo momento, eseguire di nuovo questo cmdlet e specificare questo parametro.</span><span class="sxs-lookup"><span data-stu-id="563df-120">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="563df-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="563df-121">-Confirm</span></span>
<span data-ttu-id="563df-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="563df-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="563df-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="563df-123">-WhatIf</span></span>
<span data-ttu-id="563df-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="563df-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="563df-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="563df-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="563df-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="563df-126">CommonParameters</span></span>
<span data-ttu-id="563df-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="563df-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="563df-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="563df-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="563df-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="563df-129">INPUTS</span></span>

### <span data-ttu-id="563df-130">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupItem</span><span class="sxs-lookup"><span data-stu-id="563df-130">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem</span></span>
<span data-ttu-id="563df-131">Parameters: Item (ByValue)</span><span class="sxs-lookup"><span data-stu-id="563df-131">Parameters: Item (ByValue)</span></span>

## <span data-ttu-id="563df-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="563df-132">OUTPUTS</span></span>

### <span data-ttu-id="563df-133">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="563df-133">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="563df-134">Note</span><span class="sxs-lookup"><span data-stu-id="563df-134">NOTES</span></span>

## <span data-ttu-id="563df-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="563df-135">RELATED LINKS</span></span>

[<span data-ttu-id="563df-136">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="563df-136">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="563df-137">Get-AzureRmBackupItem</span><span class="sxs-lookup"><span data-stu-id="563df-137">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)


