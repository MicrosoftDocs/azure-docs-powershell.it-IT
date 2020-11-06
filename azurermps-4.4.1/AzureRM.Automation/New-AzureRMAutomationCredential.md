---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
ms.openlocfilehash: cb332c1aed8f828f893417561302ddcf36ba0cdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517116"
---
# <span data-ttu-id="e49e6-101">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e49e6-101">New-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="e49e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e49e6-102">SYNOPSIS</span></span>
<span data-ttu-id="e49e6-103">Crea una credenziale di automazione.</span><span class="sxs-lookup"><span data-stu-id="e49e6-103">Creates an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e49e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e49e6-104">SYNTAX</span></span>

```
New-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e49e6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e49e6-105">DESCRIPTION</span></span>
<span data-ttu-id="e49e6-106">Il cmdlet **New-AzureRmAutomationCredential** crea una credenziale come oggetto **PSCredential** in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e49e6-106">The **New-AzureRmAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="e49e6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e49e6-107">EXAMPLES</span></span>

### <span data-ttu-id="e49e6-108">Esempio 1: creare una credenziale</span><span class="sxs-lookup"><span data-stu-id="e49e6-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e49e6-109">Il primo comando assegna un nome utente alla variabile $User.</span><span class="sxs-lookup"><span data-stu-id="e49e6-109">The first command assigns a user name to the $User variable.</span></span>

<span data-ttu-id="e49e6-110">Il secondo comando converte una password di testo normale in una stringa sicura usando il cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="e49e6-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="e49e6-111">Il comando Archivia l'oggetto nella variabile $Password.</span><span class="sxs-lookup"><span data-stu-id="e49e6-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="e49e6-112">Il terzo comando crea una credenziale basata su $User e $Password e quindi la archivia nella variabile $Credential.</span><span class="sxs-lookup"><span data-stu-id="e49e6-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>

<span data-ttu-id="e49e6-113">Il comando finale crea una credenziale di automazione denominata ContosoCredential che usa $Credential.</span><span class="sxs-lookup"><span data-stu-id="e49e6-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="e49e6-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e49e6-114">PARAMETERS</span></span>

### <span data-ttu-id="e49e6-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e49e6-115">-AutomationAccountName</span></span>
<span data-ttu-id="e49e6-116">Specifica il nome dell'account di automazione in cui questo cmdlet archivia le credenziali.</span><span class="sxs-lookup"><span data-stu-id="e49e6-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="e49e6-117">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="e49e6-117">-Description</span></span>
<span data-ttu-id="e49e6-118">Specifica una descrizione per la credenziale.</span><span class="sxs-lookup"><span data-stu-id="e49e6-118">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="e49e6-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="e49e6-119">-Name</span></span>
<span data-ttu-id="e49e6-120">Specifica un nome per la credenziale.</span><span class="sxs-lookup"><span data-stu-id="e49e6-120">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="e49e6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e49e6-121">-ResourceGroupName</span></span>
<span data-ttu-id="e49e6-122">Specifica una descrizione per il gruppo di risorse per cui questo cmdlet crea una credenziale.</span><span class="sxs-lookup"><span data-stu-id="e49e6-122">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="e49e6-123">-Valore</span><span class="sxs-lookup"><span data-stu-id="e49e6-123">-Value</span></span>
<span data-ttu-id="e49e6-124">Specifica le credenziali come oggetto **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="e49e6-124">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="e49e6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e49e6-125">-DefaultProfile</span></span>
<span data-ttu-id="e49e6-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e49e6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e49e6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e49e6-127">CommonParameters</span></span>
<span data-ttu-id="e49e6-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e49e6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e49e6-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e49e6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e49e6-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e49e6-130">INPUTS</span></span>

## <span data-ttu-id="e49e6-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e49e6-131">OUTPUTS</span></span>

### <span data-ttu-id="e49e6-132">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="e49e6-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="e49e6-133">Note</span><span class="sxs-lookup"><span data-stu-id="e49e6-133">NOTES</span></span>

## <span data-ttu-id="e49e6-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e49e6-134">RELATED LINKS</span></span>

[<span data-ttu-id="e49e6-135">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e49e6-135">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="e49e6-136">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e49e6-136">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="e49e6-137">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e49e6-137">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


