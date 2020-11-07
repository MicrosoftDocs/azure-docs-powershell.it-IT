---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 410d78df47a37daa90213056170c86f24c423986
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855625"
---
# <span data-ttu-id="4ece0-101">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="4ece0-101">Unregister-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="4ece0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ece0-102">SYNOPSIS</span></span>
<span data-ttu-id="4ece0-103">Annulla la registrazione di un server Windows o di un altro contenitore dalla volta.</span><span class="sxs-lookup"><span data-stu-id="4ece0-103">Unregisters a Windows Server or other container from the vault.</span></span>

## <span data-ttu-id="4ece0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ece0-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupContainer [-Container] <ContainerBase> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ece0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ece0-105">DESCRIPTION</span></span>
<span data-ttu-id="4ece0-106">Il cmdlet **Unregister-AzRecoveryServicesBackupContainer** Annulla la registrazione di un server Windows o di un altro contenitore di backup dalla volta.</span><span class="sxs-lookup"><span data-stu-id="4ece0-106">The **Unregister-AzRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="4ece0-107">Questo cmdlet consente di rimuovere i riferimenti a un contenitore dalla volta.</span><span class="sxs-lookup"><span data-stu-id="4ece0-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="4ece0-108">Prima di poter annullare la registrazione di un contenitore, è necessario eliminare tutti i dati protetti associati al contenitore.</span><span class="sxs-lookup"><span data-stu-id="4ece0-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="4ece0-109">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="4ece0-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="4ece0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ece0-110">EXAMPLES</span></span>

### <span data-ttu-id="4ece0-111">Esempio 1: annullare la registrazione di un server Windows dal Vault</span><span class="sxs-lookup"><span data-stu-id="4ece0-111">Example 1: Unregister a Windows Server from the vault</span></span>
```
PS C:\>$Cont = Get-AzRecoveryServicesBackupContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="4ece0-112">Il primo comando ottiene il contenitore di Windows denominato server01.contoso.com registrato nel Vault e lo archivia nella variabile $Cont.</span><span class="sxs-lookup"><span data-stu-id="4ece0-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>
<span data-ttu-id="4ece0-113">Il secondo comando Annulla la registrazione del server Windows specificato dall'archivio di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="4ece0-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

## <span data-ttu-id="4ece0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ece0-114">PARAMETERS</span></span>

### <span data-ttu-id="4ece0-115">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="4ece0-115">-Container</span></span>
<span data-ttu-id="4ece0-116">Specifica un oggetto contenitore di backup per annullare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="4ece0-116">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="4ece0-117">Per ottenere un oggetto **BackupContainer** , usa il cmdlet Get-AzRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="4ece0-117">To obtain a **BackupContainer** object, use the Get-AzRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ece0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ece0-118">-DefaultProfile</span></span>
<span data-ttu-id="4ece0-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ece0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ece0-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ece0-120">-PassThru</span></span>
<span data-ttu-id="4ece0-121">Restituire il contenitore da eliminare.</span><span class="sxs-lookup"><span data-stu-id="4ece0-121">Return the container to be deleted.</span></span>

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

### <span data-ttu-id="4ece0-122">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4ece0-122">-VaultId</span></span>
<span data-ttu-id="4ece0-123">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="4ece0-123">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ece0-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4ece0-124">-Confirm</span></span>
<span data-ttu-id="4ece0-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ece0-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ece0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ece0-126">-WhatIf</span></span>
<span data-ttu-id="4ece0-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ece0-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ece0-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ece0-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ece0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ece0-129">CommonParameters</span></span>
<span data-ttu-id="4ece0-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ece0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ece0-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ece0-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ece0-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ece0-132">INPUTS</span></span>

### <span data-ttu-id="4ece0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4ece0-133">System.String</span></span>

## <span data-ttu-id="4ece0-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ece0-134">OUTPUTS</span></span>

### <span data-ttu-id="4ece0-135">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="4ece0-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="4ece0-136">Note</span><span class="sxs-lookup"><span data-stu-id="4ece0-136">NOTES</span></span>

## <span data-ttu-id="4ece0-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ece0-137">RELATED LINKS</span></span>

[<span data-ttu-id="4ece0-138">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="4ece0-138">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)


