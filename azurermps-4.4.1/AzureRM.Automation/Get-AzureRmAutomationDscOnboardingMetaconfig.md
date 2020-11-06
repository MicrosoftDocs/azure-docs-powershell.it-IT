---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 58d15476921005b6da674d6a16441eb2e4f82865
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517155"
---
# <span data-ttu-id="b9856-101">Get-AzureRmAutomationDscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="b9856-101">Get-AzureRmAutomationDscOnboardingMetaconfig</span></span>

## <span data-ttu-id="b9856-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9856-102">SYNOPSIS</span></span>
<span data-ttu-id="b9856-103">Crea file MOF di meta-configurazione.</span><span class="sxs-lookup"><span data-stu-id="b9856-103">Creates meta-configuration .mof files.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9856-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9856-104">SYNTAX</span></span>

```
Get-AzureRmAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9856-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9856-105">DESCRIPTION</span></span>
<span data-ttu-id="b9856-106">Il cmdlet **Get-AzureRmAutomationDscOnboardingMetaconfig** crea i file MOF (Managed state Configuration) APS (DSC).</span><span class="sxs-lookup"><span data-stu-id="b9856-106">The **Get-AzureRmAutomationDscOnboardingMetaconfig** cmdlet creates APS Desired State Configuration (DSC) meta-configuration Managed Object Format (MOF) files.</span></span>
<span data-ttu-id="b9856-107">Questo cmdlet crea un file con estensione MOF per ogni nome di computer specificato.</span><span class="sxs-lookup"><span data-stu-id="b9856-107">This cmdlet creates a .mof file for each computer name that you specify.</span></span>
<span data-ttu-id="b9856-108">Il cmdlet crea una cartella per i file con estensione MOF.</span><span class="sxs-lookup"><span data-stu-id="b9856-108">The cmdlet creates a folder for the .mof files.</span></span>
<span data-ttu-id="b9856-109">Puoi eseguire il cmdlet Set-DscLocalConfigurationManager per questa cartella in modo che questi computer vengano imbarcati in un account di automazione di Azure come nodi DSC.</span><span class="sxs-lookup"><span data-stu-id="b9856-109">You can run the Set-DscLocalConfigurationManager cmdlet for this folder to onboard these computers into an Azure Automation account as DSC nodes.</span></span>

## <span data-ttu-id="b9856-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9856-110">EXAMPLES</span></span>

### <span data-ttu-id="b9856-111">Esempio 1: server onboard per l'automazione DSC</span><span class="sxs-lookup"><span data-stu-id="b9856-111">Example 1: Onboard servers to Automation DSC</span></span>
```
PS C:\>Get-AzureRmAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

<span data-ttu-id="b9856-112">Il primo comando crea file di configurazione di meta DSC per due server per l'account di automazione denominato Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b9856-112">The first command creates DSC meta-configuration files for two servers for the Automation account named Contoso17.</span></span>
<span data-ttu-id="b9856-113">Il comando Salva questi file su un desktop.</span><span class="sxs-lookup"><span data-stu-id="b9856-113">The command saves these files on a desktop.</span></span>

<span data-ttu-id="b9856-114">Il secondo comando usa il cmdlet **set-DscLocalConfigurationManager** per applicare la meta-configurazione ai computer specificati per inserirli come nodi DSC.</span><span class="sxs-lookup"><span data-stu-id="b9856-114">The second command uses the **Set-DscLocalConfigurationManager** cmdlet to apply the meta-configuration to the specified computers to onboard them as DSC nodes.</span></span>

## <span data-ttu-id="b9856-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9856-115">PARAMETERS</span></span>

### <span data-ttu-id="b9856-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b9856-116">-AutomationAccountName</span></span>
<span data-ttu-id="b9856-117">Specifica il nome di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="b9856-117">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="b9856-118">È possibile imbarcare i computer che il parametro *nomecomputer* specifica per l'account specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b9856-118">You can onboard the computers that the *ComputerName* parameter specifies to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="b9856-119">-Nomecomputer</span><span class="sxs-lookup"><span data-stu-id="b9856-119">-ComputerName</span></span>
<span data-ttu-id="b9856-120">Specifica una matrice di nomi di computer per cui questo cmdlet genera file con estensione MOF.</span><span class="sxs-lookup"><span data-stu-id="b9856-120">Specifies an array of names of computers for which this cmdlet generates .mof files.</span></span>
<span data-ttu-id="b9856-121">Se non specifichi questo parametro, il cmdlet genera un file con estensione MOF per il computer corrente (localhost).</span><span class="sxs-lookup"><span data-stu-id="b9856-121">If you do not specify this parameter, the cmdlet generates an .mof file for the current computer (localhost).</span></span>

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

### <span data-ttu-id="b9856-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b9856-122">-Force</span></span>
<span data-ttu-id="b9856-123">Impone l'esecuzione del comando senza richiedere conferma e per sostituire i file MOF esistenti con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="b9856-123">Forces the command to run without prompting you for confirmation, and to replace existing .mof files that have the same name.</span></span>

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

### <span data-ttu-id="b9856-124">-CartellaOutput</span><span class="sxs-lookup"><span data-stu-id="b9856-124">-OutputFolder</span></span>
<span data-ttu-id="b9856-125">Specifica il nome di una cartella in cui questo cmdlet archivia i file MOF.</span><span class="sxs-lookup"><span data-stu-id="b9856-125">Specifies the name of a folder where this cmdlet stores .mof files.</span></span>

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

### <span data-ttu-id="b9856-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9856-126">-ResourceGroupName</span></span>
<span data-ttu-id="b9856-127">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b9856-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="b9856-128">Questo cmdlet crea file MOF in computer di bordo nel gruppo di risorse specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="b9856-128">This cmdlet creates .mof files to onboard computers in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b9856-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b9856-129">-Confirm</span></span>
<span data-ttu-id="b9856-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9856-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9856-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9856-131">-WhatIf</span></span>
<span data-ttu-id="b9856-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9856-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9856-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9856-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9856-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9856-134">-DefaultProfile</span></span>
<span data-ttu-id="b9856-135">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9856-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9856-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9856-136">CommonParameters</span></span>
<span data-ttu-id="b9856-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9856-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9856-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9856-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9856-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9856-139">INPUTS</span></span>

## <span data-ttu-id="b9856-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9856-140">OUTPUTS</span></span>

### <span data-ttu-id="b9856-141">Microsoft. Azure. Commands. Automation. Model. DscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="b9856-141">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span></span>

## <span data-ttu-id="b9856-142">Note</span><span class="sxs-lookup"><span data-stu-id="b9856-142">NOTES</span></span>

## <span data-ttu-id="b9856-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9856-143">RELATED LINKS</span></span>

