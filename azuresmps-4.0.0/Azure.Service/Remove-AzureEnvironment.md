---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 4B8B56B4-511B-45BD-9595-B47187C76E03
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5af23a3ef727aa54e8223b2d07e60c2d8dbc7b8d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029939"
---
# <span data-ttu-id="f7191-101">Remove-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="f7191-101">Remove-AzureEnvironment</span></span>

## <span data-ttu-id="f7191-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7191-102">SYNOPSIS</span></span>
<span data-ttu-id="f7191-103">Elimina un ambiente Azure da Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f7191-103">Deletes an Azure environment from Windows PowerShell.</span></span>

## <span data-ttu-id="f7191-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7191-104">SYNTAX</span></span>

```
Remove-AzureEnvironment -Name <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f7191-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7191-105">DESCRIPTION</span></span>
<span data-ttu-id="f7191-106">Il cmdlet **Remove-AzureEnvironment** Elimina un ambiente Azure dal profilo comune in modo che Windows PowerShell non riesca a trovarlo.</span><span class="sxs-lookup"><span data-stu-id="f7191-106">The **Remove-AzureEnvironment** cmdlet deletes an Azure environment from your roaming profile so Windows PowerShell can't find it.</span></span>
<span data-ttu-id="f7191-107">Questo cmdlet non elimina l'ambiente da Microsoft Azure o modifica l'ambiente effettivo in alcun modo.</span><span class="sxs-lookup"><span data-stu-id="f7191-107">This cmdlet does not delete the environment from Microsoft Azure, or change the actual environment in any way.</span></span>

<span data-ttu-id="f7191-108">Un ambiente Azure una distribuzione indipendente di Microsoft Azure, ad esempio AzureCloud per Azure globale e AzureChinaCloud per Azure gestito da 21Vianet in Cina.</span><span class="sxs-lookup"><span data-stu-id="f7191-108">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="f7191-109">Puoi anche creare ambienti Azure locali usando Azure Pack e i cmdlet WAPack.</span><span class="sxs-lookup"><span data-stu-id="f7191-109">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="f7191-110">Per altre informazioni, vedere [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f7191-110">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

## <span data-ttu-id="f7191-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7191-111">EXAMPLES</span></span>

### <span data-ttu-id="f7191-112">Esempio 1: eliminare un ambiente</span><span class="sxs-lookup"><span data-stu-id="f7191-112">Example 1: Delete an environment</span></span>
```
PS C:\> Remove-AzureEnvironment -Name ContosoEnv
```

<span data-ttu-id="f7191-113">Questo comando Elimina l'ambiente ContosoEnv da Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f7191-113">This command deletes the ContosoEnv environment from Windows PowerShell.</span></span>

### <span data-ttu-id="f7191-114">Esempio 2: eliminare più ambienti</span><span class="sxs-lookup"><span data-stu-id="f7191-114">Example 2: Delete multiple environments</span></span>
```
PS C:\> Get-AzureEnvironment | Where-Object EnvironmentName -like "Contoso*" | ForEach-Object {Remove-AzureEnvironment -Name $_.EnvironmentName }
```

<span data-ttu-id="f7191-115">Questo comando Elimina gli ambienti i cui nomi iniziano con "contoso" da Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f7191-115">This command deletes environments whose names begin with "Contoso" from Windows PowerShell.</span></span>

## <span data-ttu-id="f7191-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7191-116">PARAMETERS</span></span>

### <span data-ttu-id="f7191-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f7191-117">-Force</span></span>
<span data-ttu-id="f7191-118">Elimina la richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="f7191-118">Suppresses the confirmation prompt.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7191-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7191-119">-Name</span></span>
<span data-ttu-id="f7191-120">Specifica il nome dell'ambiente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="f7191-120">Specifies the name of the environment to remove.</span></span>
<span data-ttu-id="f7191-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="f7191-121">This parameter is required.</span></span>
<span data-ttu-id="f7191-122">Questo valore di parametro fa distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="f7191-122">This parameter value is case-sensitive.</span></span>
<span data-ttu-id="f7191-123">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="f7191-123">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7191-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="f7191-124">-Profile</span></span>
<span data-ttu-id="f7191-125">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7191-125">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f7191-126">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="f7191-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7191-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7191-127">CommonParameters</span></span>
<span data-ttu-id="f7191-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7191-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7191-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7191-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7191-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7191-130">INPUTS</span></span>

### <span data-ttu-id="f7191-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f7191-131">None</span></span>
<span data-ttu-id="f7191-132">È possibile reindirizzare l'input a questo cmdlet in base al nome della proprietà, ma non in base al valore.</span><span class="sxs-lookup"><span data-stu-id="f7191-132">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="f7191-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7191-133">OUTPUTS</span></span>

### <span data-ttu-id="f7191-134">None o System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f7191-134">None or System.Boolean</span></span>
<span data-ttu-id="f7191-135">Se si usa il parametro *PassThru* , questo cmdlet restituisce un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="f7191-135">If you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="f7191-136">In caso contrario, non restituirà alcun output.</span><span class="sxs-lookup"><span data-stu-id="f7191-136">Otherwise, it does not return any output.</span></span>

## <span data-ttu-id="f7191-137">Note</span><span class="sxs-lookup"><span data-stu-id="f7191-137">NOTES</span></span>

## <span data-ttu-id="f7191-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7191-138">RELATED LINKS</span></span>

[<span data-ttu-id="f7191-139">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="f7191-139">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="f7191-140">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="f7191-140">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="f7191-141">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="f7191-141">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


