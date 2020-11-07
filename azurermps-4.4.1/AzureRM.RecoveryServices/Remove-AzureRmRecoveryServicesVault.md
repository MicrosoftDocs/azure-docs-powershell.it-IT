---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: b3df84865d29bbcf62074c1b1ed7f5586fb64fee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687102"
---
# <span data-ttu-id="d3ccc-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="d3ccc-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="d3ccc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3ccc-102">SYNOPSIS</span></span>
<span data-ttu-id="d3ccc-103">Elimina un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d3ccc-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3ccc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3ccc-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3ccc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3ccc-105">DESCRIPTION</span></span>
<span data-ttu-id="d3ccc-106">Il cmdlet **Remove-AzureRmRecoveryServicesVault** Elimina un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d3ccc-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="d3ccc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3ccc-107">EXAMPLES</span></span>

## <span data-ttu-id="d3ccc-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3ccc-108">PARAMETERS</span></span>

### <span data-ttu-id="d3ccc-109">-Vault</span><span class="sxs-lookup"><span data-stu-id="d3ccc-109">-Vault</span></span>
<span data-ttu-id="d3ccc-110">Specifica un oggetto Vault di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="d3ccc-110">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="d3ccc-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d3ccc-111">-Confirm</span></span>
<span data-ttu-id="d3ccc-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3ccc-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3ccc-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3ccc-113">-WhatIf</span></span>
<span data-ttu-id="d3ccc-114">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3ccc-114">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3ccc-115">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3ccc-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3ccc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3ccc-116">-DefaultProfile</span></span>
<span data-ttu-id="d3ccc-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3ccc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3ccc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3ccc-118">CommonParameters</span></span>
<span data-ttu-id="d3ccc-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3ccc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3ccc-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3ccc-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3ccc-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3ccc-121">INPUTS</span></span>

### <span data-ttu-id="d3ccc-122">ARSVault</span><span class="sxs-lookup"><span data-stu-id="d3ccc-122">ARSVault</span></span>
<span data-ttu-id="d3ccc-123">Il parametro "Vault" accetta il valore di tipo "ARSVault" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d3ccc-123">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="d3ccc-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3ccc-124">OUTPUTS</span></span>

### <span data-ttu-id="d3ccc-125">Microsoft. Azure. Commands. RecoveryServices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="d3ccc-125">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="d3ccc-126">Note</span><span class="sxs-lookup"><span data-stu-id="d3ccc-126">NOTES</span></span>

## <span data-ttu-id="d3ccc-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3ccc-127">RELATED LINKS</span></span>

[<span data-ttu-id="d3ccc-128">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="d3ccc-128">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="d3ccc-129">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="d3ccc-129">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="d3ccc-130">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="d3ccc-130">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)


