---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 922BEA08-6619-4D4C-86EC-58279C9E1D93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Unregister-AzureRmBackupContainer.md
ms.openlocfilehash: 41209f3790b7520c50e3105f9ca7c4a5a0e79dfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688370"
---
# <span data-ttu-id="363dc-101">Unregister-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="363dc-101">Unregister-AzureRmBackupContainer</span></span>

## <span data-ttu-id="363dc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="363dc-102">SYNOPSIS</span></span>
<span data-ttu-id="363dc-103">Annulla la registrazione di un contenitore da un caveau di backup.</span><span class="sxs-lookup"><span data-stu-id="363dc-103">Unregisters a container from a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="363dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="363dc-104">SYNTAX</span></span>

```
Unregister-AzureRmBackupContainer [-Force] [-Container] <AzureRMBackupContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="363dc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="363dc-105">DESCRIPTION</span></span>
<span data-ttu-id="363dc-106">Il cmdlet **Unregister-AzureRmBackupContainer** Annulla la registrazione della macchina virtuale Windows Server o Azure da un Vault di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="363dc-106">The **Unregister-AzureRmBackupContainer** cmdlet unregisters the Windows Server or Azure virtual machine from an Azure Backup vault.</span></span>
<span data-ttu-id="363dc-107">Questo cmdlet consente di rimuovere i riferimenti a un contenitore dall'archivio di backup.</span><span class="sxs-lookup"><span data-stu-id="363dc-107">This cmdlet removes references to a container from the Backup vault.</span></span>
<span data-ttu-id="363dc-108">Prima di poter annullare la registrazione di un contenitore, è necessario eliminare tutti i dati protetti associati al contenitore.</span><span class="sxs-lookup"><span data-stu-id="363dc-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

## <span data-ttu-id="363dc-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="363dc-109">EXAMPLES</span></span>

### <span data-ttu-id="363dc-110">Esempio 1: annullare la registrazione di un server Windows</span><span class="sxs-lookup"><span data-stu-id="363dc-110">Example 1: Unregister a Windows Server</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Container = Get-AzureRmBackupContainer -Vault $Vault -Type Windows -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmBackupContainer -Container $Container[0]
Unregister Server
This operation will delete all data in the backup vault that is associated with the server. Are you sure you want to unregister the server? 
[] Yes  [] No  [?] Help (default is "No"): Yes
```

<span data-ttu-id="363dc-111">Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="363dc-111">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="363dc-112">Il comando Archivia l'oggetto nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="363dc-112">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="363dc-113">Il secondo comando ottiene un contenitore con il nome specificato nel Vault in $Vault usando il cmdlet Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="363dc-113">The second command gets a container that has the specified name in the vault in $Vault by using the Get-AzureRmBackupContainer cmdlet.</span></span>
<span data-ttu-id="363dc-114">Il comando Archivia l'oggetto nella variabile $Container.</span><span class="sxs-lookup"><span data-stu-id="363dc-114">The command stores that object in the $Container variable.</span></span>

<span data-ttu-id="363dc-115">Il comando finale annulla la registrazione del server Windows specificato dall'archivio di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="363dc-115">The final command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

### <span data-ttu-id="363dc-116">Esempio 2: annullare la registrazione di un server Windows senza conferma</span><span class="sxs-lookup"><span data-stu-id="363dc-116">Example 2: Unregister a Windows Server without confirmation</span></span>
```
PS C:\>Unregister-AzureRmBackupContainer -Container $Container[0] -Force
```

<span data-ttu-id="363dc-117">Questo comando Annulla la registrazione del server Windows specificato dall'archivio di backup di Azure, così come nel primo esempio.</span><span class="sxs-lookup"><span data-stu-id="363dc-117">This command unregisters the specified Windows Server from the Azure Backup vault, just as in the first example.</span></span>
<span data-ttu-id="363dc-118">Questo comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="363dc-118">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="363dc-119">Di conseguenza, il comando non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="363dc-119">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="363dc-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="363dc-120">PARAMETERS</span></span>

### <span data-ttu-id="363dc-121">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="363dc-121">-Container</span></span>
<span data-ttu-id="363dc-122">Specifica la macchina virtuale Windows Server o Azure che il cmdlet Annulla la registrazione.</span><span class="sxs-lookup"><span data-stu-id="363dc-122">Specifies the Windows Server or Azure virtual machine that this cmdlet unregisters.</span></span>
<span data-ttu-id="363dc-123">Per ottenere un **AzureRmBackupContainer** , usare il cmdlet Get-AzureRmBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="363dc-123">To obtain an **AzureRmBackupContainer** , use the Get-AzureRmBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="363dc-124">-Force</span><span class="sxs-lookup"><span data-stu-id="363dc-124">-Force</span></span>
<span data-ttu-id="363dc-125">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="363dc-125">Forces the command to run without asking for user confirmation.</span></span>
<span data-ttu-id="363dc-126">Questo parametro è pertinente solo per gli oggetti **AzureBackupContainer** di tipo Windows.</span><span class="sxs-lookup"><span data-stu-id="363dc-126">This parameter is relevant only for **AzureBackupContainer** objects of type Windows.</span></span>

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

### <span data-ttu-id="363dc-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="363dc-127">-Confirm</span></span>
<span data-ttu-id="363dc-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="363dc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="363dc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="363dc-129">-WhatIf</span></span>
<span data-ttu-id="363dc-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="363dc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="363dc-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="363dc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="363dc-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="363dc-132">-DefaultProfile</span></span>
<span data-ttu-id="363dc-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="363dc-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="363dc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="363dc-134">CommonParameters</span></span>
<span data-ttu-id="363dc-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="363dc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="363dc-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="363dc-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="363dc-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="363dc-137">INPUTS</span></span>

### <span data-ttu-id="363dc-138">AzureBackupContainer</span><span class="sxs-lookup"><span data-stu-id="363dc-138">AzureBackupContainer</span></span>

## <span data-ttu-id="363dc-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="363dc-139">OUTPUTS</span></span>

### <span data-ttu-id="363dc-140">AzureBackupJob</span><span class="sxs-lookup"><span data-stu-id="363dc-140">AzureBackupJob</span></span>
<span data-ttu-id="363dc-141">Questo cmdlet restituisce $Null se il tipo di contenitore è Windows Server.</span><span class="sxs-lookup"><span data-stu-id="363dc-141">This cmdlet returns $Null if the container type is Windows Server.</span></span>

## <span data-ttu-id="363dc-142">Note</span><span class="sxs-lookup"><span data-stu-id="363dc-142">NOTES</span></span>
* <span data-ttu-id="363dc-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="363dc-143">None</span></span>

## <span data-ttu-id="363dc-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="363dc-144">RELATED LINKS</span></span>

[<span data-ttu-id="363dc-145">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="363dc-145">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="363dc-146">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="363dc-146">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="363dc-147">Registro-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="363dc-147">Register-AzureRmBackupContainer</span></span>](./Register-AzureRmBackupContainer.md)


