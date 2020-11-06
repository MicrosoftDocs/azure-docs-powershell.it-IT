---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/unregister-azurermrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: 6ad62049600f1734beabcc1a322086aad1a92348
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518055"
---
# <span data-ttu-id="6a2c0-101">Unregister-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="6a2c0-101">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="6a2c0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a2c0-102">SYNOPSIS</span></span>
<span data-ttu-id="6a2c0-103">Annulla la registrazione di un server Windows o di un altro contenitore dalla volta.</span><span class="sxs-lookup"><span data-stu-id="6a2c0-103">Unregisters a Windows Server or other container from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a2c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a2c0-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupContainer [-Container] <ContainerBase> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a2c0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a2c0-105">DESCRIPTION</span></span>
<span data-ttu-id="6a2c0-106">Il cmdlet **Unregister-AzureRmRecoveryServicesBackupContainer** Annulla la registrazione di un server Windows o di un altro contenitore di backup dalla volta.</span><span class="sxs-lookup"><span data-stu-id="6a2c0-106">The **Unregister-AzureRmRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="6a2c0-107">Questo cmdlet consente di rimuovere i riferimenti a un contenitore dalla volta.</span><span class="sxs-lookup"><span data-stu-id="6a2c0-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="6a2c0-108">Prima di poter annullare la registrazione di un contenitore, è necessario eliminare tutti i dati protetti associati al contenitore.</span><span class="sxs-lookup"><span data-stu-id="6a2c0-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="6a2c0-109">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="6a2c0-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="6a2c0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a2c0-110">EXAMPLES</span></span>

### <span data-ttu-id="6a2c0-111">Esempio 1: annullare la registrazione di un server Windows dal Vault</span><span class="sxs-lookup"><span data-stu-id="6a2c0-111">Example 1: Unregister a Windows Server from the vault</span></span>
```
PS C:\>$Cont = Get-AzureRmRecoveryServicesContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="6a2c0-112">Il primo comando ottiene il contenitore di Windows denominato server01.contoso.com registrato nel Vault e lo archivia nella variabile $Cont.</span><span class="sxs-lookup"><span data-stu-id="6a2c0-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>

<span data-ttu-id="6a2c0-113">Il secondo comando Annulla la registrazione del server Windows specificato dall'archivio di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="6a2c0-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

## <span data-ttu-id="6a2c0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a2c0-114">PARAMETERS</span></span>

### <span data-ttu-id="6a2c0-115">-Contenitore</span><span class="sxs-lookup"><span data-stu-id="6a2c0-115">-Container</span></span>
<span data-ttu-id="6a2c0-116">Specifica un oggetto contenitore di backup per annullare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="6a2c0-116">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="6a2c0-117">Per ottenere un oggetto **BackupContainer** , usa il cmdlet Get-AzureRmRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="6a2c0-117">To obtain a **BackupContainer** object, use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: ContainerBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a2c0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a2c0-118">-DefaultProfile</span></span>
<span data-ttu-id="6a2c0-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a2c0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a2c0-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a2c0-120">-PassThru</span></span>
<span data-ttu-id="6a2c0-121">Restituire il contenitore da eliminare.</span><span class="sxs-lookup"><span data-stu-id="6a2c0-121">Return the container to be deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a2c0-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6a2c0-122">-Confirm</span></span>
<span data-ttu-id="6a2c0-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a2c0-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a2c0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a2c0-124">-WhatIf</span></span>
<span data-ttu-id="6a2c0-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a2c0-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a2c0-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a2c0-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a2c0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a2c0-127">CommonParameters</span></span>
<span data-ttu-id="6a2c0-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a2c0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a2c0-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a2c0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a2c0-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a2c0-130">INPUTS</span></span>

### <span data-ttu-id="6a2c0-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6a2c0-131">None</span></span>
<span data-ttu-id="6a2c0-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="6a2c0-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6a2c0-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a2c0-133">OUTPUTS</span></span>

## <span data-ttu-id="6a2c0-134">Note</span><span class="sxs-lookup"><span data-stu-id="6a2c0-134">NOTES</span></span>

## <span data-ttu-id="6a2c0-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a2c0-135">RELATED LINKS</span></span>

[<span data-ttu-id="6a2c0-136">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="6a2c0-136">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)


