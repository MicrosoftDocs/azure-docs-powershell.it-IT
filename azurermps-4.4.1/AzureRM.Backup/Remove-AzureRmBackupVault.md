---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 698DCD00-13C0-4C36-A74B-35215D608339
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
ms.openlocfilehash: 8530dbff2e348f1b068afe7293cae9c993ce064e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517071"
---
# <span data-ttu-id="e3c1f-101">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="e3c1f-101">Remove-AzureRmBackupVault</span></span>

## <span data-ttu-id="e3c1f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="e3c1f-103">Elimina un caveau di backup.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-103">Deletes a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3c1f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3c1f-104">SYNTAX</span></span>

```
Remove-AzureRmBackupVault [-Force] [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3c1f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3c1f-105">DESCRIPTION</span></span>
<span data-ttu-id="e3c1f-106">Il cmdlet **Remove-AzureRmBackupVault** Elimina un Vault di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-106">The **Remove-AzureRmBackupVault** cmdlet deletes an Azure Backup vault.</span></span>

<span data-ttu-id="e3c1f-107">Prima di poter eliminare un archivio di backup, è necessario che sia vuoto.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-107">Before you can delete a Backup vault, it must be empty.</span></span>
<span data-ttu-id="e3c1f-108">Usa il cmdlet **Remove-AzureRmBackupContainer** per rimuovere i dati di backup della macchina virtuale dell'infrastruttura come servizio (IaaS) dalla volta.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-108">Use the **Remove-AzureRmBackupContainer** cmdlet to remove infrastructure as a service (IaaS) virtual machine backup data from the vault.</span></span>
<span data-ttu-id="e3c1f-109">Usare il cmdlet **delete-registeredserver** per rimuovere altri server registrati e i dati di backup.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-109">Use the **Delete-RegisteredServer** cmdlet to remove other registered servers and backup data.</span></span>

## <span data-ttu-id="e3c1f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3c1f-110">EXAMPLES</span></span>

### <span data-ttu-id="e3c1f-111">Esempio 1: eliminare un Vault di backup di Azure</span><span class="sxs-lookup"><span data-stu-id="e3c1f-111">Example 1: Delete an Azure Backup vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Remove-AzureRmBackupVault
```

<span data-ttu-id="e3c1f-112">Questo comando ottiene il Vault di backup di Azure denominato Vault03 usando il cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="e3c1f-112">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="e3c1f-113">Il comando passa il Vault al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-113">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e3c1f-114">Il cmdlet corrente rimuove il Vault.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-114">The current cmdlet removes the vault.</span></span>

## <span data-ttu-id="e3c1f-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3c1f-115">PARAMETERS</span></span>

### <span data-ttu-id="e3c1f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="e3c1f-116">-Force</span></span>
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

### <span data-ttu-id="e3c1f-117">-Vault</span><span class="sxs-lookup"><span data-stu-id="e3c1f-117">-Vault</span></span>
<span data-ttu-id="e3c1f-118">Specifica un archivio di backup rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-118">Specifies a Backup vault that this cmdlet removes.</span></span>
<span data-ttu-id="e3c1f-119">Per ottenere un **AzureRmBackupVault** , usare il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-119">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="e3c1f-120">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e3c1f-120">-Confirm</span></span>
<span data-ttu-id="e3c1f-121">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3c1f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3c1f-122">-WhatIf</span></span>
<span data-ttu-id="e3c1f-123">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3c1f-124">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3c1f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3c1f-125">-DefaultProfile</span></span>
<span data-ttu-id="e3c1f-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3c1f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3c1f-127">CommonParameters</span></span>
<span data-ttu-id="e3c1f-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3c1f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3c1f-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3c1f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3c1f-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3c1f-130">INPUTS</span></span>

### <span data-ttu-id="e3c1f-131">AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="e3c1f-131">AzureRMBackupVault</span></span>

## <span data-ttu-id="e3c1f-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3c1f-132">OUTPUTS</span></span>

### <span data-ttu-id="e3c1f-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e3c1f-133">None</span></span>

## <span data-ttu-id="e3c1f-134">Note</span><span class="sxs-lookup"><span data-stu-id="e3c1f-134">NOTES</span></span>
* <span data-ttu-id="e3c1f-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e3c1f-135">None</span></span>

## <span data-ttu-id="e3c1f-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3c1f-136">RELATED LINKS</span></span>

[<span data-ttu-id="e3c1f-137">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="e3c1f-137">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="e3c1f-138">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="e3c1f-138">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="e3c1f-139">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="e3c1f-139">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


