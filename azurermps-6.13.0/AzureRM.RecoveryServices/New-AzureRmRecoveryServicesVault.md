---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/new-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: 08166ea1ebe4c78521a68f9e5423a7947e78b699
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520878"
---
# <span data-ttu-id="11b6a-101">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="11b6a-101">New-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="11b6a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="11b6a-102">SYNOPSIS</span></span>
<span data-ttu-id="11b6a-103">Crea un nuovo Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="11b6a-103">Creates a new Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11b6a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="11b6a-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11b6a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="11b6a-105">DESCRIPTION</span></span>
<span data-ttu-id="11b6a-106">Il cmdlet **New-AzureRmRecoveryServicesVault** crea un nuovo Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="11b6a-106">The **New-AzureRmRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="11b6a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="11b6a-107">EXAMPLES</span></span>

### <span data-ttu-id="11b6a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="11b6a-108">Example 1</span></span>
```
PS C:\> New-AzureRmRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="11b6a-109">Creare un Vault del servizio di recupero nel gruppo di risorse e nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="11b6a-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="11b6a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="11b6a-110">PARAMETERS</span></span>

### <span data-ttu-id="11b6a-111">-Posizione</span><span class="sxs-lookup"><span data-stu-id="11b6a-111">-Location</span></span>
<span data-ttu-id="11b6a-112">Specifica il nome della posizione geografica del Vault.</span><span class="sxs-lookup"><span data-stu-id="11b6a-112">Specifies the name of the geographic location of the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11b6a-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="11b6a-113">-Name</span></span>
<span data-ttu-id="11b6a-114">Specifica il nome del Vault da creare.</span><span class="sxs-lookup"><span data-stu-id="11b6a-114">Specifies the name of the vault to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11b6a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11b6a-115">-ResourceGroupName</span></span>
<span data-ttu-id="11b6a-116">Specifica il nome del gruppo di risorse Azure in cui creare o da cui recuperare l'oggetto servizi di ripristino specificato.</span><span class="sxs-lookup"><span data-stu-id="11b6a-116">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11b6a-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="11b6a-117">-Confirm</span></span>
<span data-ttu-id="11b6a-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11b6a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11b6a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11b6a-119">-WhatIf</span></span>
<span data-ttu-id="11b6a-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="11b6a-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11b6a-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="11b6a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11b6a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11b6a-122">-DefaultProfile</span></span>
<span data-ttu-id="11b6a-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="11b6a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11b6a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b6a-124">CommonParameters</span></span>
<span data-ttu-id="11b6a-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11b6a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b6a-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11b6a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b6a-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="11b6a-127">INPUTS</span></span>

### <span data-ttu-id="11b6a-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="11b6a-128">None</span></span>

## <span data-ttu-id="11b6a-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="11b6a-129">OUTPUTS</span></span>

### <span data-ttu-id="11b6a-130">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="11b6a-130">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="11b6a-131">Note</span><span class="sxs-lookup"><span data-stu-id="11b6a-131">NOTES</span></span>

## <span data-ttu-id="11b6a-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="11b6a-132">RELATED LINKS</span></span>

[<span data-ttu-id="11b6a-133">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="11b6a-133">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="11b6a-134">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="11b6a-134">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="11b6a-135">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="11b6a-135">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


