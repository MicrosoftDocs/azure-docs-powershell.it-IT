---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
ms.openlocfilehash: 59a1b7bc849767f8d7d389631a69ae1fc93dc759
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687653"
---
# <span data-ttu-id="013f4-101">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="013f4-101">New-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="013f4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="013f4-102">SYNOPSIS</span></span>
<span data-ttu-id="013f4-103">Crea una credenziale di automazione.</span><span class="sxs-lookup"><span data-stu-id="013f4-103">Creates an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="013f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="013f4-104">SYNTAX</span></span>

```
New-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="013f4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="013f4-105">DESCRIPTION</span></span>
<span data-ttu-id="013f4-106">Il cmdlet **New-AzureRmAutomationCredential** crea una credenziale come oggetto **PSCredential** in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="013f4-106">The **New-AzureRmAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="013f4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="013f4-107">EXAMPLES</span></span>

### <span data-ttu-id="013f4-108">Esempio 1: creare una credenziale</span><span class="sxs-lookup"><span data-stu-id="013f4-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="013f4-109">Il primo comando assegna un nome utente alla variabile $User.</span><span class="sxs-lookup"><span data-stu-id="013f4-109">The first command assigns a user name to the $User variable.</span></span>

<span data-ttu-id="013f4-110">Il secondo comando converte una password di testo normale in una stringa sicura usando il cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="013f4-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="013f4-111">Il comando Archivia l'oggetto nella variabile $Password.</span><span class="sxs-lookup"><span data-stu-id="013f4-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="013f4-112">Il terzo comando crea una credenziale basata su $User e $Password e quindi la archivia nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="013f4-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>

<span data-ttu-id="013f4-113">Il comando finale crea una credenziale di automazione denominata ContosoCredential che usa $Credential.</span><span class="sxs-lookup"><span data-stu-id="013f4-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="013f4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="013f4-114">PARAMETERS</span></span>

### <span data-ttu-id="013f4-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="013f4-115">-AutomationAccountName</span></span>
<span data-ttu-id="013f4-116">Specifica il nome dell'account di automazione in cui questo cmdlet archivia le credenziali.</span><span class="sxs-lookup"><span data-stu-id="013f4-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="013f4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="013f4-117">-DefaultProfile</span></span>
<span data-ttu-id="013f4-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="013f4-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="013f4-119">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="013f4-119">-Description</span></span>
<span data-ttu-id="013f4-120">Specifica una descrizione per la credenziale.</span><span class="sxs-lookup"><span data-stu-id="013f4-120">Specifies a description for the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="013f4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="013f4-121">-Name</span></span>
<span data-ttu-id="013f4-122">Specifica un nome per la credenziale.</span><span class="sxs-lookup"><span data-stu-id="013f4-122">Specifies a name for the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="013f4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="013f4-123">-ResourceGroupName</span></span>
<span data-ttu-id="013f4-124">Specifica una descrizione per il gruppo di risorse per cui questo cmdlet crea una credenziale.</span><span class="sxs-lookup"><span data-stu-id="013f4-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="013f4-125">-Valore</span><span class="sxs-lookup"><span data-stu-id="013f4-125">-Value</span></span>
<span data-ttu-id="013f4-126">Specifica le credenziali come oggetto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="013f4-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="013f4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="013f4-127">CommonParameters</span></span>
<span data-ttu-id="013f4-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="013f4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="013f4-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="013f4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="013f4-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="013f4-130">INPUTS</span></span>

### <span data-ttu-id="013f4-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="013f4-131">None</span></span>
<span data-ttu-id="013f4-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="013f4-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="013f4-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="013f4-133">OUTPUTS</span></span>

### <span data-ttu-id="013f4-134">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="013f4-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="013f4-135">Note</span><span class="sxs-lookup"><span data-stu-id="013f4-135">NOTES</span></span>

## <span data-ttu-id="013f4-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="013f4-136">RELATED LINKS</span></span>

[<span data-ttu-id="013f4-137">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="013f4-137">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="013f4-138">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="013f4-138">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="013f4-139">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="013f4-139">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


