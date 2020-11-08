---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
ms.openlocfilehash: e44b9a5c497aba5533d53acdc9aab31cb5ece703
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033312"
---
# <span data-ttu-id="3ec90-101">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3ec90-101">Set-AzAutomationCredential</span></span>

## <span data-ttu-id="3ec90-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3ec90-102">SYNOPSIS</span></span>
<span data-ttu-id="3ec90-103">Modifica una credenziale di automazione.</span><span class="sxs-lookup"><span data-stu-id="3ec90-103">Modifies an Automation credential.</span></span>

## <span data-ttu-id="3ec90-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3ec90-104">SYNTAX</span></span>

```
Set-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ec90-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ec90-105">DESCRIPTION</span></span>
<span data-ttu-id="3ec90-106">Il cmdlet **set-AzAutomationCredential** modifica una credenziale come oggetto **PSCredential** in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3ec90-106">The **Set-AzAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="3ec90-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3ec90-107">EXAMPLES</span></span>

### <span data-ttu-id="3ec90-108">Esempio 1: aggiornare una credenziale</span><span class="sxs-lookup"><span data-stu-id="3ec90-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="3ec90-109">Il primo comando assegna un nome utente alla variabile $User.</span><span class="sxs-lookup"><span data-stu-id="3ec90-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="3ec90-110">Il secondo comando converte una password di testo normale in una stringa sicura usando il cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="3ec90-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="3ec90-111">Il comando Archivia l'oggetto nella variabile $Password.</span><span class="sxs-lookup"><span data-stu-id="3ec90-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="3ec90-112">Il terzo comando crea una credenziale basata su $User e $Password e quindi la archivia nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="3ec90-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="3ec90-113">Il comando finale modifica le credenziali di automazione denominate ContosoCredential per l'utilizzo delle credenziali in $Credential.</span><span class="sxs-lookup"><span data-stu-id="3ec90-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="3ec90-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3ec90-114">PARAMETERS</span></span>

### <span data-ttu-id="3ec90-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3ec90-115">-AutomationAccountName</span></span>
<span data-ttu-id="3ec90-116">Specifica il nome dell'account di automazione per cui questo cmdlet modifica una credenziale.</span><span class="sxs-lookup"><span data-stu-id="3ec90-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="3ec90-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ec90-117">-DefaultProfile</span></span>
<span data-ttu-id="3ec90-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3ec90-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ec90-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ec90-119">-Description</span></span>
<span data-ttu-id="3ec90-120">Specifica una descrizione per le credenziali modificate da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ec90-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3ec90-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="3ec90-121">-Name</span></span>
<span data-ttu-id="3ec90-122">Specifica il nome delle credenziali modificate da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ec90-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="3ec90-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ec90-123">-ResourceGroupName</span></span>
<span data-ttu-id="3ec90-124">Specifica il nome del gruppo di risorse per cui questo cmdlet modifica una credenziale.</span><span class="sxs-lookup"><span data-stu-id="3ec90-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="3ec90-125">-Valore</span><span class="sxs-lookup"><span data-stu-id="3ec90-125">-Value</span></span>
<span data-ttu-id="3ec90-126">Specifica le credenziali come oggetto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="3ec90-126">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="3ec90-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ec90-127">CommonParameters</span></span>
<span data-ttu-id="3ec90-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ec90-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ec90-129">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ec90-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ec90-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3ec90-130">INPUTS</span></span>

### <span data-ttu-id="3ec90-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3ec90-131">System.String</span></span>

### <span data-ttu-id="3ec90-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="3ec90-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="3ec90-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3ec90-133">OUTPUTS</span></span>

### <span data-ttu-id="3ec90-134">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="3ec90-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="3ec90-135">Note</span><span class="sxs-lookup"><span data-stu-id="3ec90-135">NOTES</span></span>

## <span data-ttu-id="3ec90-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3ec90-136">RELATED LINKS</span></span>

[<span data-ttu-id="3ec90-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3ec90-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="3ec90-138">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3ec90-138">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="3ec90-139">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="3ec90-139">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)


