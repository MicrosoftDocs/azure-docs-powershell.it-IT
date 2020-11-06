---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 34ce74bcaf61c4d0801bfb62fe15a45469a4c149
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507684"
---
# <span data-ttu-id="3dfec-101">Get-AzureRmAutomationDscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="3dfec-101">Get-AzureRmAutomationDscOnboardingMetaconfig</span></span>

## <span data-ttu-id="3dfec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3dfec-102">SYNOPSIS</span></span>
<span data-ttu-id="3dfec-103">Crea file MOF di meta-configurazione.</span><span class="sxs-lookup"><span data-stu-id="3dfec-103">Creates meta-configuration .mof files.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dfec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3dfec-104">SYNTAX</span></span>

```
Get-AzureRmAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dfec-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3dfec-105">DESCRIPTION</span></span>
<span data-ttu-id="3dfec-106">Il cmdlet **Get-AzureRmAutomationDscOnboardingMetaconfig** crea i file MOF (Managed state Configuration) APS (DSC).</span><span class="sxs-lookup"><span data-stu-id="3dfec-106">The **Get-AzureRmAutomationDscOnboardingMetaconfig** cmdlet creates APS Desired State Configuration (DSC) meta-configuration Managed Object Format (MOF) files.</span></span>
<span data-ttu-id="3dfec-107">Questo cmdlet crea un file con estensione MOF per ogni nome di computer specificato.</span><span class="sxs-lookup"><span data-stu-id="3dfec-107">This cmdlet creates a .mof file for each computer name that you specify.</span></span>
<span data-ttu-id="3dfec-108">Il cmdlet crea una cartella per i file con estensione MOF.</span><span class="sxs-lookup"><span data-stu-id="3dfec-108">The cmdlet creates a folder for the .mof files.</span></span>
<span data-ttu-id="3dfec-109">Puoi eseguire il cmdlet Set-DscLocalConfigurationManager per questa cartella in modo che questi computer vengano imbarcati in un account di automazione di Azure come nodi DSC.</span><span class="sxs-lookup"><span data-stu-id="3dfec-109">You can run the Set-DscLocalConfigurationManager cmdlet for this folder to onboard these computers into an Azure Automation account as DSC nodes.</span></span>

## <span data-ttu-id="3dfec-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3dfec-110">EXAMPLES</span></span>

### <span data-ttu-id="3dfec-111">Esempio 1: server onboard per l'automazione DSC</span><span class="sxs-lookup"><span data-stu-id="3dfec-111">Example 1: Onboard servers to Automation DSC</span></span>
```
PS C:\>Get-AzureRmAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

<span data-ttu-id="3dfec-112">Il primo comando crea file di configurazione di meta DSC per due server per l'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3dfec-112">The first command creates DSC meta-configuration files for two servers for the Automation account named Contoso17.</span></span>
<span data-ttu-id="3dfec-113">Il comando Salva questi file su un desktop.</span><span class="sxs-lookup"><span data-stu-id="3dfec-113">The command saves these files on a desktop.</span></span>
<span data-ttu-id="3dfec-114">Il secondo comando usa il cmdlet **set-DscLocalConfigurationManager** per applicare la meta-configurazione ai computer specificati per inserirli come nodi DSC.</span><span class="sxs-lookup"><span data-stu-id="3dfec-114">The second command uses the **Set-DscLocalConfigurationManager** cmdlet to apply the meta-configuration to the specified computers to onboard them as DSC nodes.</span></span>

## <span data-ttu-id="3dfec-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3dfec-115">PARAMETERS</span></span>

### <span data-ttu-id="3dfec-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3dfec-116">-AutomationAccountName</span></span>
<span data-ttu-id="3dfec-117">Specifica il nome di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="3dfec-117">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="3dfec-118">È possibile imbarcare i computer che il parametro *nomecomputer* specifica per l'account specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3dfec-118">You can onboard the computers that the *ComputerName* parameter specifies to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="3dfec-119">-Nomecomputer</span><span class="sxs-lookup"><span data-stu-id="3dfec-119">-ComputerName</span></span>
<span data-ttu-id="3dfec-120">Specifica una matrice di nomi di computer per cui questo cmdlet genera file con estensione MOF.</span><span class="sxs-lookup"><span data-stu-id="3dfec-120">Specifies an array of names of computers for which this cmdlet generates .mof files.</span></span>
<span data-ttu-id="3dfec-121">Se non specifichi questo parametro, il cmdlet genera un file con estensione MOF per il computer corrente (localhost).</span><span class="sxs-lookup"><span data-stu-id="3dfec-121">If you do not specify this parameter, the cmdlet generates an .mof file for the current computer (localhost).</span></span>

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

### <span data-ttu-id="3dfec-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dfec-122">-DefaultProfile</span></span>
<span data-ttu-id="3dfec-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3dfec-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3dfec-124">-Force</span><span class="sxs-lookup"><span data-stu-id="3dfec-124">-Force</span></span>
<span data-ttu-id="3dfec-125">Impone l'esecuzione del comando senza richiedere conferma e per sostituire i file MOF esistenti con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="3dfec-125">Forces the command to run without prompting you for confirmation, and to replace existing .mof files that have the same name.</span></span>

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

### <span data-ttu-id="3dfec-126">-CartellaOutput</span><span class="sxs-lookup"><span data-stu-id="3dfec-126">-OutputFolder</span></span>
<span data-ttu-id="3dfec-127">Specifica il nome di una cartella in cui questo cmdlet archivia i file MOF.</span><span class="sxs-lookup"><span data-stu-id="3dfec-127">Specifies the name of a folder where this cmdlet stores .mof files.</span></span>

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

### <span data-ttu-id="3dfec-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dfec-128">-ResourceGroupName</span></span>
<span data-ttu-id="3dfec-129">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3dfec-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="3dfec-130">Questo cmdlet crea file MOF in computer di bordo nel gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="3dfec-130">This cmdlet creates .mof files to onboard computers in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3dfec-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3dfec-131">-Confirm</span></span>
<span data-ttu-id="3dfec-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dfec-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dfec-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dfec-133">-WhatIf</span></span>
<span data-ttu-id="3dfec-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3dfec-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dfec-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3dfec-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dfec-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dfec-136">CommonParameters</span></span>
<span data-ttu-id="3dfec-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dfec-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dfec-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dfec-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dfec-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3dfec-139">INPUTS</span></span>

### <span data-ttu-id="3dfec-140">System. String</span><span class="sxs-lookup"><span data-stu-id="3dfec-140">System.String</span></span>

### <span data-ttu-id="3dfec-141">System. String []</span><span class="sxs-lookup"><span data-stu-id="3dfec-141">System.String[]</span></span>

## <span data-ttu-id="3dfec-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3dfec-142">OUTPUTS</span></span>

### <span data-ttu-id="3dfec-143">Microsoft. Azure. Commands. Automation. Model. DscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="3dfec-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span></span>

## <span data-ttu-id="3dfec-144">Note</span><span class="sxs-lookup"><span data-stu-id="3dfec-144">NOTES</span></span>

## <span data-ttu-id="3dfec-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3dfec-145">RELATED LINKS</span></span>