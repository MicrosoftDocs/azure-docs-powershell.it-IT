---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: a0f21fc8cde4c64eaf1e8ea27bf05eff8d664c55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677580"
---
# <span data-ttu-id="e87e4-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e87e4-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="e87e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e87e4-102">SYNOPSIS</span></span>
<span data-ttu-id="e87e4-103">Elimina un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e87e4-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="e87e4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e87e4-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e87e4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e87e4-105">DESCRIPTION</span></span>
<span data-ttu-id="e87e4-106">Il cmdlet **Remove-AzRecoveryServicesVault** Elimina un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e87e4-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="e87e4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e87e4-107">EXAMPLES</span></span>

### <span data-ttu-id="e87e4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e87e4-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="e87e4-109">Elimina un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="e87e4-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="e87e4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e87e4-110">PARAMETERS</span></span>

### <span data-ttu-id="e87e4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e87e4-111">-DefaultProfile</span></span>
<span data-ttu-id="e87e4-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e87e4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e87e4-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="e87e4-113">-Vault</span></span>
<span data-ttu-id="e87e4-114">Specifica un oggetto Vault di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="e87e4-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="e87e4-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e87e4-115">-Confirm</span></span>
<span data-ttu-id="e87e4-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e87e4-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e87e4-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e87e4-117">-WhatIf</span></span>
<span data-ttu-id="e87e4-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e87e4-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e87e4-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e87e4-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e87e4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e87e4-120">CommonParameters</span></span>
<span data-ttu-id="e87e4-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e87e4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e87e4-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e87e4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e87e4-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e87e4-123">INPUTS</span></span>

### <span data-ttu-id="e87e4-124">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="e87e4-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="e87e4-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e87e4-125">OUTPUTS</span></span>

### <span data-ttu-id="e87e4-126">Microsoft. Azure. Commands. RecoveryServices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="e87e4-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="e87e4-127">Note</span><span class="sxs-lookup"><span data-stu-id="e87e4-127">NOTES</span></span>

## <span data-ttu-id="e87e4-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e87e4-128">RELATED LINKS</span></span>

[<span data-ttu-id="e87e4-129">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e87e4-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="e87e4-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="e87e4-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="e87e4-131">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e87e4-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


