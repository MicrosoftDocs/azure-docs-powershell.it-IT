---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/set-azurermrecoveryservicesbackupproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
ms.openlocfilehash: 7fa55bd306a1cbe04ddf3af63a66682a0fa17f1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509139"
---
# <span data-ttu-id="a1fb6-101">Set-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="a1fb6-101">Set-AzureRmRecoveryServicesBackupProperties</span></span>

## <span data-ttu-id="a1fb6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1fb6-102">SYNOPSIS</span></span>
<span data-ttu-id="a1fb6-103">Imposta le proprietà per la gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="a1fb6-103">Sets the properties for backup management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1fb6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1fb6-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProperties -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1fb6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1fb6-105">DESCRIPTION</span></span>
<span data-ttu-id="a1fb6-106">Il cmdlet **set-AzureRmRecoveryServicesBackupProperties** imposta le proprietà di archiviazione di backup per un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="a1fb6-106">The **Set-AzureRmRecoveryServicesBackupProperties** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="a1fb6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1fb6-107">EXAMPLES</span></span>

### <span data-ttu-id="a1fb6-108">Esempio 1: impostare lo spazio di archiviazione georidondante per un Vault</span><span class="sxs-lookup"><span data-stu-id="a1fb6-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzureRmRecoveryServicesBackupProperties -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="a1fb6-109">Il primo comando ottiene il Vault denominato TestVault e lo archivia nella variabile $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="a1fb6-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="a1fb6-110">Il secondo comando imposta la ridondanza dello spazio di archiviazione di backup per $Vault 01 su georidondante.</span><span class="sxs-lookup"><span data-stu-id="a1fb6-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="a1fb6-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1fb6-111">PARAMETERS</span></span>

### <span data-ttu-id="a1fb6-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="a1fb6-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="a1fb6-113">Specifica il tipo di ridondanza dello spazio di archiviazione di backup.</span><span class="sxs-lookup"><span data-stu-id="a1fb6-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: AzureRmRecoveryServicesBackupStorageRedundancyType
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1fb6-114">-Vault</span><span class="sxs-lookup"><span data-stu-id="a1fb6-114">-Vault</span></span>
<span data-ttu-id="a1fb6-115">Specifica il nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="a1fb6-115">Specifies the name of the vault.</span></span>
<span data-ttu-id="a1fb6-116">Il Vault deve essere un oggetto **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="a1fb6-116">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1fb6-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a1fb6-117">-Confirm</span></span>
<span data-ttu-id="a1fb6-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1fb6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1fb6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1fb6-119">-WhatIf</span></span>
<span data-ttu-id="a1fb6-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1fb6-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1fb6-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1fb6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1fb6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1fb6-122">-DefaultProfile</span></span>
<span data-ttu-id="a1fb6-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1fb6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1fb6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1fb6-124">CommonParameters</span></span>
<span data-ttu-id="a1fb6-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1fb6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1fb6-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1fb6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1fb6-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1fb6-127">INPUTS</span></span>

### <span data-ttu-id="a1fb6-128">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="a1fb6-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="a1fb6-129">Parameters: Vault (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a1fb6-129">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="a1fb6-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1fb6-130">OUTPUTS</span></span>

### <span data-ttu-id="a1fb6-131">System. void</span><span class="sxs-lookup"><span data-stu-id="a1fb6-131">System.Void</span></span>

## <span data-ttu-id="a1fb6-132">Note</span><span class="sxs-lookup"><span data-stu-id="a1fb6-132">NOTES</span></span>

## <span data-ttu-id="a1fb6-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1fb6-133">RELATED LINKS</span></span>

[<span data-ttu-id="a1fb6-134">Get-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="a1fb6-134">Get-AzureRmRecoveryServicesBackupProperties</span></span>](./Get-AzureRmRecoveryServicesBackupProperties.md)

[<span data-ttu-id="a1fb6-135">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="a1fb6-135">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

