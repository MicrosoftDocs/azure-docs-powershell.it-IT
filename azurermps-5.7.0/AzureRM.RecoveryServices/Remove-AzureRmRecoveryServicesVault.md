---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/remove-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 4d3046827a7d3338833b0c8c788cfb7a9e18bc2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519384"
---
# <span data-ttu-id="bff16-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="bff16-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="bff16-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bff16-102">SYNOPSIS</span></span>
<span data-ttu-id="bff16-103">Elimina un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="bff16-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bff16-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bff16-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bff16-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bff16-105">DESCRIPTION</span></span>
<span data-ttu-id="bff16-106">Il cmdlet **Remove-AzureRmRecoveryServicesVault** Elimina un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="bff16-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="bff16-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bff16-107">EXAMPLES</span></span>

### <span data-ttu-id="bff16-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bff16-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="bff16-109">Elimina un Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="bff16-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="bff16-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bff16-110">PARAMETERS</span></span>

### <span data-ttu-id="bff16-111">-Vault</span><span class="sxs-lookup"><span data-stu-id="bff16-111">-Vault</span></span>
<span data-ttu-id="bff16-112">Specifica un oggetto Vault di ripristino di Azure site.</span><span class="sxs-lookup"><span data-stu-id="bff16-112">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="bff16-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bff16-113">-Confirm</span></span>
<span data-ttu-id="bff16-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bff16-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bff16-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bff16-115">-WhatIf</span></span>
<span data-ttu-id="bff16-116">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bff16-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bff16-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bff16-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bff16-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff16-118">-DefaultProfile</span></span>
<span data-ttu-id="bff16-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bff16-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bff16-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff16-120">CommonParameters</span></span>
<span data-ttu-id="bff16-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bff16-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff16-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bff16-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff16-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bff16-123">INPUTS</span></span>

### <span data-ttu-id="bff16-124">ARSVault</span><span class="sxs-lookup"><span data-stu-id="bff16-124">ARSVault</span></span>
<span data-ttu-id="bff16-125">Il parametro "Vault" accetta il valore di tipo "ARSVault" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="bff16-125">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="bff16-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bff16-126">OUTPUTS</span></span>

### <span data-ttu-id="bff16-127">Microsoft. Azure. Commands. RecoveryServices. VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="bff16-127">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="bff16-128">Note</span><span class="sxs-lookup"><span data-stu-id="bff16-128">NOTES</span></span>

## <span data-ttu-id="bff16-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bff16-129">RELATED LINKS</span></span>

[<span data-ttu-id="bff16-130">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="bff16-130">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="bff16-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="bff16-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="bff16-132">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="bff16-132">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)


