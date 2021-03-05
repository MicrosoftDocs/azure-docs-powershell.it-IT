---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 5e66fc57f6ee9daffde27226bc0321f415cc10d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997414"
---
# <span data-ttu-id="9d440-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="9d440-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="9d440-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d440-102">SYNOPSIS</span></span>
<span data-ttu-id="9d440-103">Imposta le proprietà per la gestione del backup.</span><span class="sxs-lookup"><span data-stu-id="9d440-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="9d440-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d440-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>  [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-EnableCrossRegionRestore] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d440-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9d440-105">DESCRIPTION</span></span>
<span data-ttu-id="9d440-106">Il cmdlet **Set-AzRecoveryServicesBackupProperty** imposta le proprietà di archiviazione di backup per un vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="9d440-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="9d440-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d440-107">EXAMPLES</span></span>

### <span data-ttu-id="9d440-108">Esempio 1: Impostare lo spazio di archiviazione GeoRedundant per un vault</span><span class="sxs-lookup"><span data-stu-id="9d440-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="9d440-109">Il primo comando recupera il vault denominato TestVault e quindi lo archivia nella variabile $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="9d440-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="9d440-110">Il secondo comando imposta la ridondanza dello spazio di archiviazione di backup per $Vault 01 su GeoRedundant.</span><span class="sxs-lookup"><span data-stu-id="9d440-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="9d440-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d440-111">PARAMETERS</span></span>

### <span data-ttu-id="9d440-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="9d440-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="9d440-113">Specifica il tipo di ridondanza dello spazio di archiviazione di backup.</span><span class="sxs-lookup"><span data-stu-id="9d440-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.AzureRmRecoveryServicesBackupStorageRedundancyType]
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, ZoneRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d440-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d440-114">-DefaultProfile</span></span>
<span data-ttu-id="9d440-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d440-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d440-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="9d440-116">-Vault</span></span>
<span data-ttu-id="9d440-117">Specifica il nome del vault.</span><span class="sxs-lookup"><span data-stu-id="9d440-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="9d440-118">Il vault deve essere un **oggetto AzureRmRecoveryServicesVault.**</span><span class="sxs-lookup"><span data-stu-id="9d440-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="9d440-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d440-119">-Confirm</span></span>
<span data-ttu-id="9d440-120">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d440-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d440-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d440-121">-WhatIf</span></span>
<span data-ttu-id="9d440-122">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9d440-122">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="9d440-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d440-123">CommonParameters</span></span>
<span data-ttu-id="9d440-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d440-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d440-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9d440-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d440-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="9d440-126">INPUTS</span></span>

### <span data-ttu-id="9d440-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="9d440-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="9d440-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d440-128">OUTPUTS</span></span>

### <span data-ttu-id="9d440-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="9d440-129">System.Void</span></span>

## <span data-ttu-id="9d440-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="9d440-130">NOTES</span></span>

## <span data-ttu-id="9d440-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d440-131">RELATED LINKS</span></span>

[<span data-ttu-id="9d440-132">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="9d440-132">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="9d440-133">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="9d440-133">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)


