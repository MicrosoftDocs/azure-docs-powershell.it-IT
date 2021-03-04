---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 9591E150-54DA-48B7-8656-3891833FE61E
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesVault.md
ms.openlocfilehash: 811ac8b9f8922844dd5153a4fa02abc4c023f7a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953309"
---
# <span data-ttu-id="72821-101">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="72821-101">New-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="72821-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72821-102">SYNOPSIS</span></span>
<span data-ttu-id="72821-103">Crea un nuovo vault di Servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="72821-103">Creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="72821-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72821-104">SYNTAX</span></span>

```
New-AzRecoveryServicesVault -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72821-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="72821-105">DESCRIPTION</span></span>
<span data-ttu-id="72821-106">Il cmdlet **New-AzRecoveryServicesVault** crea un nuovo vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="72821-106">The **New-AzRecoveryServicesVault** cmdlet creates a new Recovery Services vault.</span></span>

## <span data-ttu-id="72821-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72821-107">EXAMPLES</span></span>

### <span data-ttu-id="72821-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="72821-108">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesVault -Name "vaultName" -ResourceGroupName "rg" -Location "eastasia"
```

<span data-ttu-id="72821-109">Creare il vault del servizio di ripristino nel gruppo di risorse e nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="72821-109">Create recovery service vault in resource group and given location.</span></span>

## <span data-ttu-id="72821-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72821-110">PARAMETERS</span></span>

### <span data-ttu-id="72821-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72821-111">-DefaultProfile</span></span>
<span data-ttu-id="72821-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72821-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72821-113">-Location</span><span class="sxs-lookup"><span data-stu-id="72821-113">-Location</span></span>
<span data-ttu-id="72821-114">Specifica il nome della posizione geografica del vault.</span><span class="sxs-lookup"><span data-stu-id="72821-114">Specifies the name of the geographic location of the vault.</span></span>

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

### <span data-ttu-id="72821-115">-Name</span><span class="sxs-lookup"><span data-stu-id="72821-115">-Name</span></span>
<span data-ttu-id="72821-116">Specifica il nome del vault da creare.</span><span class="sxs-lookup"><span data-stu-id="72821-116">Specifies the name of the vault to create.</span></span>

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

### <span data-ttu-id="72821-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72821-117">-ResourceGroupName</span></span>
<span data-ttu-id="72821-118">Specifica il nome del gruppo di risorse azure in cui creare o da cui recuperare l'oggetto dei servizi di ripristino specificato.</span><span class="sxs-lookup"><span data-stu-id="72821-118">Specifies the name of the Azure resource group in which to create or from which to retrieve the specified Recovery Services object.</span></span>

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

### <span data-ttu-id="72821-119">-Tag</span><span class="sxs-lookup"><span data-stu-id="72821-119">-Tag</span></span>

<span data-ttu-id="72821-120">Specifica i tag da aggiungere al Vault dei servizi di ripristino</span><span class="sxs-lookup"><span data-stu-id="72821-120">Specifies the Tags to add to the Recovery Services Vault</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72821-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="72821-121">-Confirm</span></span>
<span data-ttu-id="72821-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72821-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72821-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72821-123">-WhatIf</span></span>
<span data-ttu-id="72821-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72821-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72821-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72821-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72821-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72821-126">CommonParameters</span></span>
<span data-ttu-id="72821-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72821-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72821-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="72821-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72821-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="72821-129">INPUTS</span></span>

### <span data-ttu-id="72821-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="72821-130">None</span></span>

## <span data-ttu-id="72821-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72821-131">OUTPUTS</span></span>

### <span data-ttu-id="72821-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="72821-132">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="72821-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="72821-133">NOTES</span></span>

## <span data-ttu-id="72821-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72821-134">RELATED LINKS</span></span>

[<span data-ttu-id="72821-135">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="72821-135">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="72821-136">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="72821-136">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="72821-137">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="72821-137">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)


