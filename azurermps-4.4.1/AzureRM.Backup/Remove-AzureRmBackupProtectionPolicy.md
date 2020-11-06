---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 189E3DD8-AA43-4D4C-A873-971E0585E54E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 80b03c8ba4bab5968e55dff40633b014a586d450
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517079"
---
# <span data-ttu-id="9e6e4-101">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9e6e4-101">Remove-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="9e6e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e6e4-102">SYNOPSIS</span></span>
<span data-ttu-id="9e6e4-103">Elimina un criterio da un caveau di backup.</span><span class="sxs-lookup"><span data-stu-id="9e6e4-103">Deletes a policy from a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e6e4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e6e4-104">SYNTAX</span></span>

```
Remove-AzureRmBackupProtectionPolicy [-Force] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e6e4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e6e4-105">DESCRIPTION</span></span>
<span data-ttu-id="9e6e4-106">Il cmdlet **Remove-AzureRmBackupProtectionPolicy** Elimina un criterio da un Vault di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="9e6e4-106">The **Remove-AzureRmBackupProtectionPolicy** cmdlet deletes a policy from an Azure Backup vault.</span></span>

<span data-ttu-id="9e6e4-107">Prima di poter eliminare un criterio di protezione del backup, il criterio non deve contenere elementi di backup associati.</span><span class="sxs-lookup"><span data-stu-id="9e6e4-107">Before you can delete a backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="9e6e4-108">Prima di eliminare il criterio, verificare che ogni elemento associato sia associato ad altri criteri.</span><span class="sxs-lookup"><span data-stu-id="9e6e4-108">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="9e6e4-109">Per associare un altro criterio a un elemento di backup, usare il cmdlet Enable-AzureRmBackupProtection.</span><span class="sxs-lookup"><span data-stu-id="9e6e4-109">To associate another policy with a backup item, use the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="9e6e4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e6e4-110">EXAMPLES</span></span>

### <span data-ttu-id="9e6e4-111">Esempio 1: rimuovere un criterio di protezione del backup</span><span class="sxs-lookup"><span data-stu-id="9e6e4-111">Example 1: Remove a backup protection policy</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DailyBackup" | Remove-AzureRmBackupProtectionPolicy
```

<span data-ttu-id="9e6e4-112">Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="9e6e4-112">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="9e6e4-113">Il comando Archivia l'oggetto nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="9e6e4-113">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="9e6e4-114">Il secondo comando crea un criterio di conservazione per 30 giorni di conservazione giornaliera e lo archivia nella variabile $Daily.</span><span class="sxs-lookup"><span data-stu-id="9e6e4-114">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="9e6e4-115">Il secondo comando ottiene i criteri di protezione denominati BackupGiornaliero nel Vault in $Vault usando il cmdlet **Get-AzureRmBackupProtectionPolicy** .</span><span class="sxs-lookup"><span data-stu-id="9e6e4-115">The second command gets the protection policy named DailyBackup in the vault in $Vault by using the **Get-AzureRmBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="9e6e4-116">Il comando passa il criterio al cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="9e6e4-116">The command passes the policy to the current cmdlet.</span></span>
<span data-ttu-id="9e6e4-117">Questo cmdlet rimuove i criteri.</span><span class="sxs-lookup"><span data-stu-id="9e6e4-117">That cmdlet removes the policy.</span></span>

## <span data-ttu-id="9e6e4-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e6e4-118">PARAMETERS</span></span>

### <span data-ttu-id="9e6e4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9e6e4-119">-Force</span></span>
<span data-ttu-id="9e6e4-120">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9e6e4-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9e6e4-121">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9e6e4-121">-ProtectionPolicy</span></span>
<span data-ttu-id="9e6e4-122">Specifica i criteri di protezione rimossi da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e6e4-122">Specifies protection policy that this cmdlet removes.</span></span>
<span data-ttu-id="9e6e4-123">Per ottenere un **AzureRmBackupProtectionPolicy** , usare il cmdlet Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9e6e4-123">To obtain an **AzureRmBackupProtectionPolicy** , use the Get-AzureRmBackupProtectionPolicy cmdlet</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e6e4-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9e6e4-124">-Confirm</span></span>
<span data-ttu-id="9e6e4-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e6e4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e6e4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e6e4-126">-WhatIf</span></span>
<span data-ttu-id="9e6e4-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e6e4-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e6e4-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9e6e4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e6e4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e6e4-129">-DefaultProfile</span></span>
<span data-ttu-id="9e6e4-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e6e4-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e6e4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e6e4-131">CommonParameters</span></span>
<span data-ttu-id="9e6e4-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e6e4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e6e4-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e6e4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e6e4-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e6e4-134">INPUTS</span></span>

### <span data-ttu-id="9e6e4-135">AzureRMBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9e6e4-135">AzureRMBackupProtectionPolicy</span></span>

## <span data-ttu-id="9e6e4-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e6e4-136">OUTPUTS</span></span>

### <span data-ttu-id="9e6e4-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9e6e4-137">None</span></span>

## <span data-ttu-id="9e6e4-138">Note</span><span class="sxs-lookup"><span data-stu-id="9e6e4-138">NOTES</span></span>

## <span data-ttu-id="9e6e4-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e6e4-139">RELATED LINKS</span></span>

[<span data-ttu-id="9e6e4-140">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="9e6e4-140">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="9e6e4-141">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9e6e4-141">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="9e6e4-142">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9e6e4-142">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


