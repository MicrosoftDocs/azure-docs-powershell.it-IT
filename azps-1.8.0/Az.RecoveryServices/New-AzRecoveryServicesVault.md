---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
ms.openlocfilehash: 65694116a924759c4cf29a7abcf95da7a03df39f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677607"
---
# <span data-ttu-id="5c059-101">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="5c059-101">New-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="5c059-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5c059-102">SYNOPSIS</span></span>
<span data-ttu-id="5c059-103">Crea un nuovo Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5c059-103">Creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="5c059-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c059-104">SYNTAX</span></span>

```
New-AzRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c059-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c059-105">DESCRIPTION</span></span>
<span data-ttu-id="5c059-106">Il cmdlet **New-AzRecoveryServicesVault** crea un nuovo Vault di servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="5c059-106">The **New-AzRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="5c059-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c059-107">EXAMPLES</span></span>

### <span data-ttu-id="5c059-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5c059-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="5c059-109">Creare un Vault del servizio di recupero nel gruppo di risorse e nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="5c059-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="5c059-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5c059-110">PARAMETERS</span></span>

### <span data-ttu-id="5c059-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c059-111">-DefaultProfile</span></span>
<span data-ttu-id="5c059-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5c059-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c059-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5c059-113">-Location</span></span>
<span data-ttu-id="5c059-114">Specifica il nome della posizione geografica del Vault.</span><span class="sxs-lookup"><span data-stu-id="5c059-114">Specifies the name of the geographic location of the vault.</span></span>

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

### <span data-ttu-id="5c059-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c059-115">-Name</span></span>
<span data-ttu-id="5c059-116">Specifica il nome del Vault da creare.</span><span class="sxs-lookup"><span data-stu-id="5c059-116">Specifies the name of the vault to create.</span></span>

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

### <span data-ttu-id="5c059-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c059-117">-ResourceGroupName</span></span>
<span data-ttu-id="5c059-118">Specifica il nome del gruppo di risorse Azure in cui creare o da cui recuperare l'oggetto servizi di ripristino specificato.</span><span class="sxs-lookup"><span data-stu-id="5c059-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="5c059-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5c059-119">-Confirm</span></span>
<span data-ttu-id="5c059-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c059-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c059-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c059-121">-WhatIf</span></span>
<span data-ttu-id="5c059-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c059-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c059-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c059-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c059-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c059-124">CommonParameters</span></span>
<span data-ttu-id="5c059-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c059-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c059-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c059-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c059-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5c059-127">INPUTS</span></span>

### <span data-ttu-id="5c059-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5c059-128">None</span></span>

## <span data-ttu-id="5c059-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c059-129">OUTPUTS</span></span>

### <span data-ttu-id="5c059-130">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="5c059-130">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="5c059-131">Note</span><span class="sxs-lookup"><span data-stu-id="5c059-131">NOTES</span></span>

## <span data-ttu-id="5c059-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c059-132">RELATED LINKS</span></span>

[<span data-ttu-id="5c059-133">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="5c059-133">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="5c059-134">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="5c059-134">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="5c059-135">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="5c059-135">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


