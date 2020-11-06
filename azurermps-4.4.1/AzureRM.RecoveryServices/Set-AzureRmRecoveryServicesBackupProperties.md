---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
ms.openlocfilehash: bb4009edce4e447daacd4cd32835bebc8655dba1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513055"
---
# <span data-ttu-id="5ccd4-101">Set-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="5ccd4-101">Set-AzureRmRecoveryServicesBackupProperties</span></span>

## <span data-ttu-id="5ccd4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5ccd4-102">SYNOPSIS</span></span>
<span data-ttu-id="5ccd4-103">Imposta le proprietà per la gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="5ccd4-103">Sets the properties for backup management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ccd4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5ccd4-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProperties -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ccd4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5ccd4-105">DESCRIPTION</span></span>
<span data-ttu-id="5ccd4-106">Il cmdlet **set-AzureRmRecoveryServicesBackupProperties** imposta le proprietà di archiviazione di backup per un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5ccd4-106">The **Set-AzureRmRecoveryServicesBackupProperties** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="5ccd4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5ccd4-107">EXAMPLES</span></span>

### <span data-ttu-id="5ccd4-108">Esempio 1: impostare lo spazio di archiviazione georidondante per un Vault</span><span class="sxs-lookup"><span data-stu-id="5ccd4-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzureRmRecoveryServicesBackupProperties -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="5ccd4-109">Il primo comando ottiene il Vault denominato TestVault e lo archivia nella variabile $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="5ccd4-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>

<span data-ttu-id="5ccd4-110">Il secondo comando imposta la ridondanza dello spazio di archiviazione di backup per $Vault 01 su georidondante.</span><span class="sxs-lookup"><span data-stu-id="5ccd4-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="5ccd4-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5ccd4-111">PARAMETERS</span></span>

### <span data-ttu-id="5ccd4-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="5ccd4-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="5ccd4-113">Specifica il tipo di ridondanza dello spazio di archiviazione di backup.</span><span class="sxs-lookup"><span data-stu-id="5ccd4-113">Specifies the backup storage redundancy type.</span></span>

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

### <span data-ttu-id="5ccd4-114">-Vault</span><span class="sxs-lookup"><span data-stu-id="5ccd4-114">-Vault</span></span>
<span data-ttu-id="5ccd4-115">Specifica il nome del Vault.</span><span class="sxs-lookup"><span data-stu-id="5ccd4-115">Specifies the name of the vault.</span></span>
<span data-ttu-id="5ccd4-116">Il Vault deve essere un oggetto **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="5ccd4-116">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="5ccd4-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5ccd4-117">-Confirm</span></span>
<span data-ttu-id="5ccd4-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ccd4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ccd4-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ccd4-119">-WhatIf</span></span>
<span data-ttu-id="5ccd4-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ccd4-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ccd4-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5ccd4-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ccd4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ccd4-122">-DefaultProfile</span></span>
<span data-ttu-id="5ccd4-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5ccd4-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ccd4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ccd4-124">CommonParameters</span></span>
<span data-ttu-id="5ccd4-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ccd4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ccd4-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ccd4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ccd4-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5ccd4-127">INPUTS</span></span>

### <span data-ttu-id="5ccd4-128">ARSVault</span><span class="sxs-lookup"><span data-stu-id="5ccd4-128">ARSVault</span></span>
<span data-ttu-id="5ccd4-129">Il parametro "Vault" accetta il valore di tipo "ARSVault" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5ccd4-129">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="5ccd4-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5ccd4-130">OUTPUTS</span></span>

## <span data-ttu-id="5ccd4-131">Note</span><span class="sxs-lookup"><span data-stu-id="5ccd4-131">NOTES</span></span>

## <span data-ttu-id="5ccd4-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5ccd4-132">RELATED LINKS</span></span>

[<span data-ttu-id="5ccd4-133">Get-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="5ccd4-133">Get-AzureRmRecoveryServicesBackupProperties</span></span>](./Get-AzureRmRecoveryServicesBackupProperties.md)

[<span data-ttu-id="5ccd4-134">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="5ccd4-134">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)


