---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
ms.openlocfilehash: 6fbef2bcedf4de93cd816f6a4702ee01df10d17f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957725"
---
# <span data-ttu-id="62044-101">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="62044-101">Set-AzAutomationCredential</span></span>

## <span data-ttu-id="62044-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62044-102">SYNOPSIS</span></span>
<span data-ttu-id="62044-103">Modifica le credenziali di automazione.</span><span class="sxs-lookup"><span data-stu-id="62044-103">Modifies an Automation credential.</span></span>

## <span data-ttu-id="62044-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62044-104">SYNTAX</span></span>

```
Set-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="62044-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="62044-105">DESCRIPTION</span></span>
<span data-ttu-id="62044-106">Il cmdlet **Set-AzAutomationCredential** modifica le credenziali come **oggetto PSCredential** nell'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="62044-106">The **Set-AzAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="62044-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62044-107">EXAMPLES</span></span>

### <span data-ttu-id="62044-108">Esempio 1: Aggiornare le credenziali</span><span class="sxs-lookup"><span data-stu-id="62044-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="62044-109">Il primo comando assegna un nome utente alla variabile $User variabile.</span><span class="sxs-lookup"><span data-stu-id="62044-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="62044-110">Il secondo comando converte una password in testo normale in una stringa sicura usando il cmdlet ConvertTo-SecureString testo.</span><span class="sxs-lookup"><span data-stu-id="62044-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="62044-111">Il comando archivia l'oggetto nella $Password variabile.</span><span class="sxs-lookup"><span data-stu-id="62044-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="62044-112">Il terzo comando crea le credenziali in $User e $Password, quindi le archivia nella variabile $Credential specificata.</span><span class="sxs-lookup"><span data-stu-id="62044-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="62044-113">Il comando finale modifica le credenziali di automazione denominate ContosoCredential per usare le credenziali in $Credential.</span><span class="sxs-lookup"><span data-stu-id="62044-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="62044-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62044-114">PARAMETERS</span></span>

### <span data-ttu-id="62044-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="62044-115">-AutomationAccountName</span></span>
<span data-ttu-id="62044-116">Specifica il nome dell'account di automazione per cui questo cmdlet modifica le credenziali.</span><span class="sxs-lookup"><span data-stu-id="62044-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="62044-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62044-117">-DefaultProfile</span></span>
<span data-ttu-id="62044-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="62044-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62044-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="62044-119">-Description</span></span>
<span data-ttu-id="62044-120">Specifica una descrizione delle credenziali che il cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="62044-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="62044-121">-Name</span><span class="sxs-lookup"><span data-stu-id="62044-121">-Name</span></span>
<span data-ttu-id="62044-122">Specifica il nome delle credenziali che il cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="62044-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="62044-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62044-123">-ResourceGroupName</span></span>
<span data-ttu-id="62044-124">Specifica il nome del gruppo di risorse per cui questo cmdlet modifica le credenziali.</span><span class="sxs-lookup"><span data-stu-id="62044-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="62044-125">-Value</span><span class="sxs-lookup"><span data-stu-id="62044-125">-Value</span></span>
<span data-ttu-id="62044-126">Specifica le credenziali come oggetto **PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="62044-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62044-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62044-127">CommonParameters</span></span>
<span data-ttu-id="62044-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62044-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62044-129">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62044-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62044-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="62044-130">INPUTS</span></span>

### <span data-ttu-id="62044-131">System.String</span><span class="sxs-lookup"><span data-stu-id="62044-131">System.String</span></span>

### <span data-ttu-id="62044-132">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="62044-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="62044-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62044-133">OUTPUTS</span></span>

### <span data-ttu-id="62044-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="62044-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="62044-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="62044-135">NOTES</span></span>

## <span data-ttu-id="62044-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62044-136">RELATED LINKS</span></span>

[<span data-ttu-id="62044-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="62044-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="62044-138">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="62044-138">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="62044-139">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="62044-139">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)


