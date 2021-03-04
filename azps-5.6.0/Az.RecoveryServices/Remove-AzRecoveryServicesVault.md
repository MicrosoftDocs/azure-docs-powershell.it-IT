---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: b3d0b292d7e680ca1d16e935c34a268cea836aeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953117"
---
# <span data-ttu-id="f57c2-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f57c2-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="f57c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f57c2-102">SYNOPSIS</span></span>
<span data-ttu-id="f57c2-103">Elimina un vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="f57c2-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="f57c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f57c2-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f57c2-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f57c2-105">DESCRIPTION</span></span>
<span data-ttu-id="f57c2-106">Il cmdlet **Remove-AzRecoveryServicesVault** elimina un vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="f57c2-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="f57c2-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f57c2-107">EXAMPLES</span></span>

### <span data-ttu-id="f57c2-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f57c2-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="f57c2-109">Elimina un vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="f57c2-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="f57c2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f57c2-110">PARAMETERS</span></span>

### <span data-ttu-id="f57c2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f57c2-111">-DefaultProfile</span></span>
<span data-ttu-id="f57c2-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f57c2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f57c2-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="f57c2-113">-Vault</span></span>
<span data-ttu-id="f57c2-114">Specifica un oggetto vault di Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f57c2-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="f57c2-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f57c2-115">-Confirm</span></span>
<span data-ttu-id="f57c2-116">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f57c2-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f57c2-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f57c2-117">-WhatIf</span></span>
<span data-ttu-id="f57c2-118">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f57c2-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f57c2-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f57c2-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f57c2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f57c2-120">CommonParameters</span></span>
<span data-ttu-id="f57c2-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f57c2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f57c2-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f57c2-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f57c2-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="f57c2-123">INPUTS</span></span>

### <span data-ttu-id="f57c2-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="f57c2-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="f57c2-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f57c2-125">OUTPUTS</span></span>

### <span data-ttu-id="f57c2-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="f57c2-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="f57c2-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="f57c2-127">NOTES</span></span>

## <span data-ttu-id="f57c2-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f57c2-128">RELATED LINKS</span></span>

[<span data-ttu-id="f57c2-129">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f57c2-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="f57c2-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f57c2-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="f57c2-131">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f57c2-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


