---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 007142cb854e2e428983f95d7bb7397c5a0ace39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182175"
---
# <span data-ttu-id="dd2f1-101">Get-AzAutomationDscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="dd2f1-101">Get-AzAutomationDscOnboardingMetaconfig</span></span>

## <span data-ttu-id="dd2f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd2f1-102">SYNOPSIS</span></span>
<span data-ttu-id="dd2f1-103">Crea file mof di metaconfigurazione.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-103">Creates meta-configuration .mof files.</span></span>

## <span data-ttu-id="dd2f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dd2f1-104">SYNTAX</span></span>

```
Get-AzAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd2f1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dd2f1-105">DESCRIPTION</span></span>
<span data-ttu-id="dd2f1-106">Il cmdlet **Get-AzAutomationDscOnboardingMetaconfig** crea file MOF (Desired State Configuration) della meta-configurazione DSC (Desired State Configuration).</span><span class="sxs-lookup"><span data-stu-id="dd2f1-106">The **Get-AzAutomationDscOnboardingMetaconfig** cmdlet creates APS Desired State Configuration (DSC) meta-configuration Managed Object Format (MOF) files.</span></span>
<span data-ttu-id="dd2f1-107">Questo cmdlet crea un file mof per ogni nome computer specificato.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-107">This cmdlet creates a .mof file for each computer name that you specify.</span></span>
<span data-ttu-id="dd2f1-108">Il cmdlet crea una cartella per i file con estensione mof.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-108">The cmdlet creates a folder for the .mof files.</span></span>
<span data-ttu-id="dd2f1-109">È possibile eseguire il cmdlet Set-DscLocalConfigurationManager per questa cartella per aggiungere questi computer a un account di automazione di Azure come nodi DSC.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-109">You can run the Set-DscLocalConfigurationManager cmdlet for this folder to onboard these computers into an Azure Automation account as DSC nodes.</span></span>

## <span data-ttu-id="dd2f1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dd2f1-110">EXAMPLES</span></span>

### <span data-ttu-id="dd2f1-111">Esempio 1: Aggiungere server all'automazione DSC</span><span class="sxs-lookup"><span data-stu-id="dd2f1-111">Example 1: Onboard servers to Automation DSC</span></span>
```
PS C:\>Get-AzAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

<span data-ttu-id="dd2f1-112">Il primo comando crea i file di meta-configurazione DSC per due server per l'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-112">The first command creates DSC meta-configuration files for two servers for the Automation account named Contoso17.</span></span>
<span data-ttu-id="dd2f1-113">Il comando salva questi file in un desktop.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-113">The command saves these files on a desktop.</span></span>
<span data-ttu-id="dd2f1-114">Il secondo comando usa il cmdlet **Set-DscLocalConfigurationManager** per applicare la metaconfigurazione ai computer specificati per onboardrli come nodi DSC.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-114">The second command uses the **Set-DscLocalConfigurationManager** cmdlet to apply the meta-configuration to the specified computers to onboard them as DSC nodes.</span></span>

## <span data-ttu-id="dd2f1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd2f1-115">PARAMETERS</span></span>

### <span data-ttu-id="dd2f1-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dd2f1-116">-AutomationAccountName</span></span>
<span data-ttu-id="dd2f1-117">Specifica il nome di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-117">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="dd2f1-118">È possibile eseguire l'onboardy dei computer specificati dal parametro *ComputerName* all'account specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-118">You can onboard the computers that the *ComputerName* parameter specifies to the account that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd2f1-119">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="dd2f1-119">-ComputerName</span></span>
<span data-ttu-id="dd2f1-120">Specifica una matrice di nomi di computer per cui questo cmdlet genera file mof.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-120">Specifies an array of names of computers for which this cmdlet generates .mof files.</span></span>
<span data-ttu-id="dd2f1-121">Se non si specifica questo parametro, il cmdlet genera un file mof per il computer corrente (localhost).</span><span class="sxs-lookup"><span data-stu-id="dd2f1-121">If you do not specify this parameter, the cmdlet generates an .mof file for the current computer (localhost).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd2f1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd2f1-122">-DefaultProfile</span></span>
<span data-ttu-id="dd2f1-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="dd2f1-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd2f1-124">-Force</span><span class="sxs-lookup"><span data-stu-id="dd2f1-124">-Force</span></span>
<span data-ttu-id="dd2f1-125">Forza l'esecuzione del comando senza chiedere conferma e sostituisce i file mof esistenti con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-125">Forces the command to run without prompting you for confirmation, and to replace existing .mof files that have the same name.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd2f1-126">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="dd2f1-126">-OutputFolder</span></span>
<span data-ttu-id="dd2f1-127">Specifica il nome di una cartella in cui il cmdlet archivia i file mof.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-127">Specifies the name of a folder where this cmdlet stores .mof files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd2f1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd2f1-128">-ResourceGroupName</span></span>
<span data-ttu-id="dd2f1-129">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="dd2f1-130">Questo cmdlet crea file mof nei computer onboard nel gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-130">This cmdlet creates .mof files to onboard computers in the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dd2f1-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dd2f1-131">-Confirm</span></span>
<span data-ttu-id="dd2f1-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd2f1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd2f1-133">-WhatIf</span></span>
<span data-ttu-id="dd2f1-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd2f1-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd2f1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd2f1-136">CommonParameters</span></span>
<span data-ttu-id="dd2f1-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd2f1-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd2f1-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd2f1-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="dd2f1-139">INPUTS</span></span>

### <span data-ttu-id="dd2f1-140">System.String</span><span class="sxs-lookup"><span data-stu-id="dd2f1-140">System.String</span></span>

### <span data-ttu-id="dd2f1-141">System.String[]</span><span class="sxs-lookup"><span data-stu-id="dd2f1-141">System.String[]</span></span>

## <span data-ttu-id="dd2f1-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dd2f1-142">OUTPUTS</span></span>

### <span data-ttu-id="dd2f1-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="dd2f1-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span></span>

## <span data-ttu-id="dd2f1-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="dd2f1-144">NOTES</span></span>

## <span data-ttu-id="dd2f1-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dd2f1-145">RELATED LINKS</span></span>
