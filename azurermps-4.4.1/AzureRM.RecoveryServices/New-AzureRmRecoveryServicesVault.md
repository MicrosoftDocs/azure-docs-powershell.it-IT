---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/New-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: d9163e42b199dd5178e37a7d1bbe22abbb05c7f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510383"
---
# <span data-ttu-id="26305-101">New-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="26305-101">New-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="26305-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26305-102">SYNOPSIS</span></span>
<span data-ttu-id="26305-103">Crea un nuovo Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="26305-103">Creates a new Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26305-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26305-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26305-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26305-105">DESCRIPTION</span></span>
<span data-ttu-id="26305-106">Il cmdlet **New-AzureRmRecoveryServicesVault** crea un nuovo Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="26305-106">The **New-AzureRmRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="26305-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26305-107">EXAMPLES</span></span>

## <span data-ttu-id="26305-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26305-108">PARAMETERS</span></span>

### <span data-ttu-id="26305-109">-Posizione</span><span class="sxs-lookup"><span data-stu-id="26305-109">-Location</span></span>
<span data-ttu-id="26305-110">Specifica il nome della posizione geografica del Vault.</span><span class="sxs-lookup"><span data-stu-id="26305-110">Specifies the name of the geographic location of the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26305-111">-Nome</span><span class="sxs-lookup"><span data-stu-id="26305-111">-Name</span></span>
<span data-ttu-id="26305-112">Specifica il nome del Vault da creare.</span><span class="sxs-lookup"><span data-stu-id="26305-112">Specifies the name of the vault to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26305-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26305-113">-ResourceGroupName</span></span>
<span data-ttu-id="26305-114">Specifica il nome del gruppo di risorse Azure in cui creare o da cui recuperare l'oggetto servizi di ripristino specificato.</span><span class="sxs-lookup"><span data-stu-id="26305-114">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26305-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="26305-115">-Confirm</span></span>
<span data-ttu-id="26305-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26305-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26305-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26305-117">-WhatIf</span></span>
<span data-ttu-id="26305-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26305-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26305-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26305-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26305-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26305-120">-DefaultProfile</span></span>
<span data-ttu-id="26305-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26305-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26305-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26305-122">CommonParameters</span></span>
<span data-ttu-id="26305-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26305-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26305-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26305-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26305-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26305-125">INPUTS</span></span>

## <span data-ttu-id="26305-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26305-126">OUTPUTS</span></span>

### <span data-ttu-id="26305-127">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="26305-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="26305-128">Note</span><span class="sxs-lookup"><span data-stu-id="26305-128">NOTES</span></span>

## <span data-ttu-id="26305-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26305-129">RELATED LINKS</span></span>

[<span data-ttu-id="26305-130">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="26305-130">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="26305-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="26305-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="26305-132">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="26305-132">Remove-AzureRmRecoveryServicesVault</span></span>](./Remove-AzureRmRecoveryServicesVault.md)


