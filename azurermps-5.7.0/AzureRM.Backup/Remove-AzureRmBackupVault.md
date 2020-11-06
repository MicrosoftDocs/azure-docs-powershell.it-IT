---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 698DCD00-13C0-4C36-A74B-35215D608339
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/remove-azurermbackupvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupVault.md
ms.openlocfilehash: 4b8098889cbec7bd313ffb2ed70c5384a7e24ef0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519934"
---
# <span data-ttu-id="7743e-101">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="7743e-101">Remove-AzureRmBackupVault</span></span>

## <span data-ttu-id="7743e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7743e-102">SYNOPSIS</span></span>
<span data-ttu-id="7743e-103">Elimina un caveau di backup.</span><span class="sxs-lookup"><span data-stu-id="7743e-103">Deletes a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7743e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7743e-104">SYNTAX</span></span>

```
Remove-AzureRmBackupVault [-Force] [-Vault] <AzureRMBackupVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7743e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7743e-105">DESCRIPTION</span></span>
<span data-ttu-id="7743e-106">Il cmdlet **Remove-AzureRmBackupVault** Elimina un Vault di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="7743e-106">The **Remove-AzureRmBackupVault** cmdlet deletes an Azure Backup vault.</span></span>

<span data-ttu-id="7743e-107">Prima di poter eliminare un archivio di backup, è necessario che sia vuoto.</span><span class="sxs-lookup"><span data-stu-id="7743e-107">Before you can delete a Backup vault, it must be empty.</span></span>
<span data-ttu-id="7743e-108">Usa il cmdlet **Remove-AzureRmBackupContainer** per rimuovere i dati di backup della macchina virtuale dell'infrastruttura come servizio (IaaS) dalla volta.</span><span class="sxs-lookup"><span data-stu-id="7743e-108">Use the **Remove-AzureRmBackupContainer** cmdlet to remove infrastructure as a service (IaaS) virtual machine backup data from the vault.</span></span>
<span data-ttu-id="7743e-109">Usare il cmdlet **delete-registeredserver** per rimuovere altri server registrati e i dati di backup.</span><span class="sxs-lookup"><span data-stu-id="7743e-109">Use the **Delete-RegisteredServer** cmdlet to remove other registered servers and backup data.</span></span>

## <span data-ttu-id="7743e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7743e-110">EXAMPLES</span></span>

### <span data-ttu-id="7743e-111">Esempio 1: eliminare un Vault di backup di Azure</span><span class="sxs-lookup"><span data-stu-id="7743e-111">Example 1: Delete an Azure Backup vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03" | Remove-AzureRmBackupVault
```

<span data-ttu-id="7743e-112">Questo comando ottiene il Vault di backup di Azure denominato Vault03 usando il cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="7743e-112">This command gets the Azure Backup vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="7743e-113">Il comando passa il Vault al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="7743e-113">The command passes that vault to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="7743e-114">Il cmdlet corrente rimuove il Vault.</span><span class="sxs-lookup"><span data-stu-id="7743e-114">The current cmdlet removes the vault.</span></span>

## <span data-ttu-id="7743e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7743e-115">PARAMETERS</span></span>

### <span data-ttu-id="7743e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7743e-116">-DefaultProfile</span></span>
<span data-ttu-id="7743e-117">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7743e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7743e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7743e-118">-Force</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7743e-119">-Vault</span><span class="sxs-lookup"><span data-stu-id="7743e-119">-Vault</span></span>
<span data-ttu-id="7743e-120">Specifica un archivio di backup rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7743e-120">Specifies a Backup vault that this cmdlet removes.</span></span>
<span data-ttu-id="7743e-121">Per ottenere un **AzureRmBackupVault** , usare il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="7743e-121">To obtain an **AzureRmBackupVault** , use the Get-AzureRmBackupVault cmdlet.</span></span>

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

### <span data-ttu-id="7743e-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7743e-122">-Confirm</span></span>
<span data-ttu-id="7743e-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7743e-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7743e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7743e-124">-WhatIf</span></span>
<span data-ttu-id="7743e-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7743e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7743e-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7743e-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7743e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7743e-127">CommonParameters</span></span>
<span data-ttu-id="7743e-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7743e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7743e-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7743e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7743e-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7743e-130">INPUTS</span></span>

### <span data-ttu-id="7743e-131">AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="7743e-131">AzureRMBackupVault</span></span>

## <span data-ttu-id="7743e-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7743e-132">OUTPUTS</span></span>

### <span data-ttu-id="7743e-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7743e-133">None</span></span>

## <span data-ttu-id="7743e-134">Note</span><span class="sxs-lookup"><span data-stu-id="7743e-134">NOTES</span></span>
* <span data-ttu-id="7743e-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7743e-135">None</span></span>

## <span data-ttu-id="7743e-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7743e-136">RELATED LINKS</span></span>

[<span data-ttu-id="7743e-137">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="7743e-137">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="7743e-138">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="7743e-138">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="7743e-139">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="7743e-139">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


