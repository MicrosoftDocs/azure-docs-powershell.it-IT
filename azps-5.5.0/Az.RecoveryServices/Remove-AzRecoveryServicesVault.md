---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: 4e6dab95f110e25f24781b2ffbd01a016bdaa9fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192855"
---
# <span data-ttu-id="7bb79-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7bb79-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="7bb79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bb79-102">SYNOPSIS</span></span>
<span data-ttu-id="7bb79-103">Elimina un vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7bb79-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="7bb79-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7bb79-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bb79-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7bb79-105">DESCRIPTION</span></span>
<span data-ttu-id="7bb79-106">Il cmdlet **Remove-AzRecoveryServicesVault** elimina un vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7bb79-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="7bb79-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7bb79-107">EXAMPLES</span></span>

### <span data-ttu-id="7bb79-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7bb79-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="7bb79-109">Elimina un vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="7bb79-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="7bb79-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bb79-110">PARAMETERS</span></span>

### <span data-ttu-id="7bb79-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bb79-111">-DefaultProfile</span></span>
<span data-ttu-id="7bb79-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7bb79-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7bb79-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="7bb79-113">-Vault</span></span>
<span data-ttu-id="7bb79-114">Specifica un oggetto vault di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7bb79-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="7bb79-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bb79-115">-Confirm</span></span>
<span data-ttu-id="7bb79-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bb79-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bb79-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bb79-117">-WhatIf</span></span>
<span data-ttu-id="7bb79-118">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7bb79-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7bb79-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7bb79-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bb79-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bb79-120">CommonParameters</span></span>
<span data-ttu-id="7bb79-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bb79-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bb79-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7bb79-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bb79-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="7bb79-123">INPUTS</span></span>

### <span data-ttu-id="7bb79-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="7bb79-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="7bb79-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7bb79-125">OUTPUTS</span></span>

### <span data-ttu-id="7bb79-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="7bb79-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="7bb79-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="7bb79-127">NOTES</span></span>

## <span data-ttu-id="7bb79-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7bb79-128">RELATED LINKS</span></span>

[<span data-ttu-id="7bb79-129">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7bb79-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="7bb79-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="7bb79-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="7bb79-131">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7bb79-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


