---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 6912f54810baeeab795e5f2efca4a51ecafe1c93
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856621"
---
# <span data-ttu-id="ee715-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="ee715-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="ee715-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee715-102">SYNOPSIS</span></span>
<span data-ttu-id="ee715-103">Imposta le proprietà per la gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="ee715-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="ee715-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee715-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee715-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee715-105">DESCRIPTION</span></span>
<span data-ttu-id="ee715-106">Il cmdlet **set-AzRecoveryServicesBackupProperty** imposta le proprietà di archiviazione di backup per un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="ee715-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="ee715-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee715-107">EXAMPLES</span></span>

### <span data-ttu-id="ee715-108">Esempio 1: impostare lo spazio di archiviazione georidondante per un Vault</span><span class="sxs-lookup"><span data-stu-id="ee715-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="ee715-109">Il primo comando ottiene il Vault denominato TestVault e lo archivia nella variabile $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="ee715-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="ee715-110">Il secondo comando imposta la ridondanza dello spazio di archiviazione di backup per $Vault 01 su georidondante.</span><span class="sxs-lookup"><span data-stu-id="ee715-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="ee715-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee715-111">PARAMETERS</span></span>

### <span data-ttu-id="ee715-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="ee715-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="ee715-113">Specifica il tipo di ridondanza dello spazio di archiviazione di backup.</span><span class="sxs-lookup"><span data-stu-id="ee715-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.AzureRmRecoveryServicesBackupStorageRedundancyType]
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee715-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee715-114">-DefaultProfile</span></span>
<span data-ttu-id="ee715-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee715-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee715-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="ee715-116">-Vault</span></span>
<span data-ttu-id="ee715-117">Specifica il nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="ee715-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="ee715-118">Il Vault deve essere un oggetto **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="ee715-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee715-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ee715-119">-Confirm</span></span>
<span data-ttu-id="ee715-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee715-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee715-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee715-121">-WhatIf</span></span>
<span data-ttu-id="ee715-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee715-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee715-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee715-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee715-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee715-124">CommonParameters</span></span>
<span data-ttu-id="ee715-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee715-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee715-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee715-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee715-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee715-127">INPUTS</span></span>

### <span data-ttu-id="ee715-128">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="ee715-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="ee715-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee715-129">OUTPUTS</span></span>

### <span data-ttu-id="ee715-130">System. void</span><span class="sxs-lookup"><span data-stu-id="ee715-130">System.Void</span></span>

## <span data-ttu-id="ee715-131">Note</span><span class="sxs-lookup"><span data-stu-id="ee715-131">NOTES</span></span>

## <span data-ttu-id="ee715-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee715-132">RELATED LINKS</span></span>

[<span data-ttu-id="ee715-133">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="ee715-133">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="ee715-134">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ee715-134">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)


