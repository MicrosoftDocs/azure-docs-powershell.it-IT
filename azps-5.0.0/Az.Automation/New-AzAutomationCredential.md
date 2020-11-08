---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
ms.openlocfilehash: a0b23cc5e16a723364d234eb2ee9723f291ee5e4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200383"
---
# <span data-ttu-id="48c6b-101">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="48c6b-101">New-AzAutomationCredential</span></span>

## <span data-ttu-id="48c6b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="48c6b-102">SYNOPSIS</span></span>
<span data-ttu-id="48c6b-103">Crea una credenziale di automazione.</span><span class="sxs-lookup"><span data-stu-id="48c6b-103">Creates an Automation credential.</span></span>

## <span data-ttu-id="48c6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="48c6b-104">SYNTAX</span></span>

```
New-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="48c6b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="48c6b-105">DESCRIPTION</span></span>
<span data-ttu-id="48c6b-106">Il cmdlet **New-AzAutomationCredential** crea una credenziale come oggetto **PSCredential** in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="48c6b-106">The **New-AzAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="48c6b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="48c6b-107">EXAMPLES</span></span>

### <span data-ttu-id="48c6b-108">Esempio 1: creare una credenziale</span><span class="sxs-lookup"><span data-stu-id="48c6b-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="48c6b-109">Il primo comando assegna un nome utente alla variabile $User.</span><span class="sxs-lookup"><span data-stu-id="48c6b-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="48c6b-110">Il secondo comando converte una password di testo normale in una stringa sicura usando il cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="48c6b-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="48c6b-111">Il comando Archivia l'oggetto nella variabile $Password.</span><span class="sxs-lookup"><span data-stu-id="48c6b-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="48c6b-112">Il terzo comando crea una credenziale basata su $User e $Password e quindi la archivia nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="48c6b-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="48c6b-113">Il comando finale crea una credenziale di automazione denominata ContosoCredential che usa $Credential.</span><span class="sxs-lookup"><span data-stu-id="48c6b-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="48c6b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="48c6b-114">PARAMETERS</span></span>

### <span data-ttu-id="48c6b-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="48c6b-115">-AutomationAccountName</span></span>
<span data-ttu-id="48c6b-116">Specifica il nome dell'account di automazione in cui questo cmdlet archivia le credenziali.</span><span class="sxs-lookup"><span data-stu-id="48c6b-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="48c6b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48c6b-117">-DefaultProfile</span></span>
<span data-ttu-id="48c6b-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="48c6b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48c6b-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="48c6b-119">-Description</span></span>
<span data-ttu-id="48c6b-120">Specifica una descrizione per la credenziale.</span><span class="sxs-lookup"><span data-stu-id="48c6b-120">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="48c6b-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="48c6b-121">-Name</span></span>
<span data-ttu-id="48c6b-122">Specifica un nome per la credenziale.</span><span class="sxs-lookup"><span data-stu-id="48c6b-122">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="48c6b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48c6b-123">-ResourceGroupName</span></span>
<span data-ttu-id="48c6b-124">Specifica una descrizione per il gruppo di risorse per cui questo cmdlet crea una credenziale.</span><span class="sxs-lookup"><span data-stu-id="48c6b-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="48c6b-125">-Valore</span><span class="sxs-lookup"><span data-stu-id="48c6b-125">-Value</span></span>
<span data-ttu-id="48c6b-126">Specifica le credenziali come oggetto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="48c6b-126">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="48c6b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48c6b-127">CommonParameters</span></span>
<span data-ttu-id="48c6b-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48c6b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48c6b-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48c6b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48c6b-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="48c6b-130">INPUTS</span></span>

### <span data-ttu-id="48c6b-131">System. String</span><span class="sxs-lookup"><span data-stu-id="48c6b-131">System.String</span></span>

### <span data-ttu-id="48c6b-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="48c6b-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="48c6b-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="48c6b-133">OUTPUTS</span></span>

### <span data-ttu-id="48c6b-134">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="48c6b-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="48c6b-135">Note</span><span class="sxs-lookup"><span data-stu-id="48c6b-135">NOTES</span></span>

## <span data-ttu-id="48c6b-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="48c6b-136">RELATED LINKS</span></span>

[<span data-ttu-id="48c6b-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="48c6b-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="48c6b-138">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="48c6b-138">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="48c6b-139">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="48c6b-139">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


