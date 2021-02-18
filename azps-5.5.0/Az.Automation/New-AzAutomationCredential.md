---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
ms.openlocfilehash: a0b23cc5e16a723364d234eb2ee9723f291ee5e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201071"
---
# <span data-ttu-id="f4dd6-101">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f4dd6-101">New-AzAutomationCredential</span></span>

## <span data-ttu-id="f4dd6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4dd6-102">SYNOPSIS</span></span>
<span data-ttu-id="f4dd6-103">Crea credenziali di automazione.</span><span class="sxs-lookup"><span data-stu-id="f4dd6-103">Creates an Automation credential.</span></span>

## <span data-ttu-id="f4dd6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4dd6-104">SYNTAX</span></span>

```
New-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4dd6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f4dd6-105">DESCRIPTION</span></span>
<span data-ttu-id="f4dd6-106">Il cmdlet **New-AzAutomationCredential** crea una credenziali come **oggetto PSCredential** nell'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f4dd6-106">The **New-AzAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="f4dd6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4dd6-107">EXAMPLES</span></span>

### <span data-ttu-id="f4dd6-108">Esempio 1: Creare le credenziali</span><span class="sxs-lookup"><span data-stu-id="f4dd6-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f4dd6-109">Il primo comando assegna un nome utente alla variabile $User variabile.</span><span class="sxs-lookup"><span data-stu-id="f4dd6-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="f4dd6-110">Il secondo comando converte una password in testo normale in una stringa sicura usando il cmdlet ConvertTo-SecureString testo.</span><span class="sxs-lookup"><span data-stu-id="f4dd6-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="f4dd6-111">Il comando archivia l'oggetto nella $Password variabile.</span><span class="sxs-lookup"><span data-stu-id="f4dd6-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="f4dd6-112">Il terzo comando crea le credenziali in $User e $Password, quindi le archivia nella variabile $Credential specificata.</span><span class="sxs-lookup"><span data-stu-id="f4dd6-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="f4dd6-113">Il comando finale crea una credenziali di automazione denominata ContosoCredential che usa $Credential.</span><span class="sxs-lookup"><span data-stu-id="f4dd6-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="f4dd6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4dd6-114">PARAMETERS</span></span>

### <span data-ttu-id="f4dd6-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f4dd6-115">-AutomationAccountName</span></span>
<span data-ttu-id="f4dd6-116">Specifica il nome dell'account di automazione in cui questo cmdlet archivia le credenziali.</span><span class="sxs-lookup"><span data-stu-id="f4dd6-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="f4dd6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4dd6-117">-DefaultProfile</span></span>
<span data-ttu-id="f4dd6-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="f4dd6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f4dd6-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4dd6-119">-Description</span></span>
<span data-ttu-id="f4dd6-120">Specifica una descrizione per le credenziali.</span><span class="sxs-lookup"><span data-stu-id="f4dd6-120">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="f4dd6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f4dd6-121">-Name</span></span>
<span data-ttu-id="f4dd6-122">Specifica un nome per le credenziali.</span><span class="sxs-lookup"><span data-stu-id="f4dd6-122">Specifies a name for the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4dd6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4dd6-123">-ResourceGroupName</span></span>
<span data-ttu-id="f4dd6-124">Specifica una descrizione per il gruppo di risorse per cui questo cmdlet crea una credenziali.</span><span class="sxs-lookup"><span data-stu-id="f4dd6-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="f4dd6-125">-Value</span><span class="sxs-lookup"><span data-stu-id="f4dd6-125">-Value</span></span>
<span data-ttu-id="f4dd6-126">Specifica le credenziali come oggetto **PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="f4dd6-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4dd6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4dd6-127">CommonParameters</span></span>
<span data-ttu-id="f4dd6-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4dd6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4dd6-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4dd6-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4dd6-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="f4dd6-130">INPUTS</span></span>

### <span data-ttu-id="f4dd6-131">System.String</span><span class="sxs-lookup"><span data-stu-id="f4dd6-131">System.String</span></span>

### <span data-ttu-id="f4dd6-132">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="f4dd6-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="f4dd6-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4dd6-133">OUTPUTS</span></span>

### <span data-ttu-id="f4dd6-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="f4dd6-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="f4dd6-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="f4dd6-135">NOTES</span></span>

## <span data-ttu-id="f4dd6-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4dd6-136">RELATED LINKS</span></span>

[<span data-ttu-id="f4dd6-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f4dd6-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="f4dd6-138">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f4dd6-138">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="f4dd6-139">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f4dd6-139">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


